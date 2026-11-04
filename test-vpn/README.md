# test-vpn

Immagine: `ghcr.io/gianlucaceci/test-vpn:latest`

## Avvio

```bash
docker compose up -d
```

## Risorse configurate

- Sistema base: almalinux
- RAM massima: 1g
- CPU massima: 1.0
- Budget gestionale dati persistenti: 20 GB
- Dati persistenti host: `/opt/COPIA/docker-projects/test-vpn/data`
- Percorso dati nel container: `/var/lib/app/data`

Il budget disco è una prenotazione gestionale del portale, non una quota fisica ext4.
Non impedisce al container di scrivere oltre il valore selezionato. Le immagini e i layer Docker
sono conservati nel Docker Root Dir configurato sul server.

## Rete

Nessuna porta pubblicata dal compose.
