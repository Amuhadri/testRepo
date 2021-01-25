CREATE DATABASE "doni-pek"
    WITH 
    OWNER = postgres
    ENCODING = 'UTF8'
    LC_COLLATE = 'Croatian_Croatia.1250'
    LC_CTYPE = 'Croatian_Croatia.1250'
    TABLESPACE = pg_default
    CONNECTION LIMIT = -1;





----

CREATE SEQUENCE public.utrosakvoltino_unos_id_seq
    INCREMENT 1
    START 1
    MINVALUE 1
    MAXVALUE 2147483647
    CACHE 1;

ALTER SEQUENCE public.utrosakvoltino_unos_id_seq
    OWNER TO postgres;
    
    
    
    ------------------
    
    CREATE TABLE public.utrosasveposlovnice
(
    unos_id integer NOT NULL DEFAULT nextval('utrosakvoltino_unos_id_seq'::regclass),
    bt550proizvodnja double precision NOT NULL,
    pt850proizvodnja double precision NOT NULL,
    ct110proizvodnja double precision NOT NULL,
    razbproizvodnja double precision NOT NULL,
    kukbproizvodnja double precision NOT NULL,
    mjesbproizvodnja double precision NOT NULL,
    posvrstebproizvodnja double precision NOT NULL,
    pecbproizvodnja double precision NOT NULL,
    ostproizvodibproizvodnja double precision NOT NULL,
    smjbproizvodnja double precision NOT NULL,
    konbproizvodnja double precision NOT NULL,
    ukupnoproizvodnja double precision NOT NULL,
    bt550potrosnja double precision NOT NULL,
    pt850potrosnja double precision NOT NULL,
    ct110potrosnja double precision NOT NULL,
    razbpotrosnja double precision NOT NULL,
    kukbpotrosnja double precision NOT NULL,
    smjbpotrosnja double precision NOT NULL,
    konbpotrosnja double precision NOT NULL,
    ukupnopotrosnja double precision NOT NULL,
    poslovnica integer NOT NULL,
    odabranidatum date,
    CONSTRAINT utrosakvoltino_pkey PRIMARY KEY (unos_id)
)

TABLESPACE pg_default;

ALTER TABLE public.utrosasveposlovnice
    OWNER to postgres;
