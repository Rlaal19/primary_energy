CREATE TABLE primary_energy_production (
    msn VARCHAR(50),
    year INT,
    month INT,
    day INT,
    ts DATE,
    value DOUBLE PRECISION,
    column_order INT,
    description VARCHAR(100),
    unit VARCHAR(50)
);


CREATE TABLE primary_energy_consumption(
    msn VARCHAR(50),
    year INT,
    month INT,
    day INT,
    ts DATE,
    value DOUBLE PRECISION,
    column_order INT,
    description VARCHAR(100),
    unit VARCHAR(50)
);


# mongoimport --collection='primary_energy_production' --db energy --type csv --headerline --file primary_energy_production.csv -u root -p example --port 27017 --authenticationDatabase admin

# mongoimport --collection='primary_energy_consumption' --db energy --type csv --headerline --file primary_energy_consumption.csv -u root -p example --port 27017 --authenticationDatabase admin


# mongorestore --archive=energy.archive.gzip --gzip --drop -u root -p example