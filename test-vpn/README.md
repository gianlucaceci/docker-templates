# test-vpn

Immagine: `ghcr.io/gianlucaceci/test-vpn:latest`

## Deploy

Avvio automatico selezionato: **sì**.

Per avviare manualmente:

```bash
docker compose up -d
```

Per fermare:

```bash
docker compose down
```

## Risorse configurate

- Sistema base: almalinux
- Pacchetti selezionati: iproute, openssh-server
- RAM massima: 1g
- CPU massima: 1.0
- Budget gestionale dati persistenti: 10 GB
- Dati persistenti host: `/opt/COPIA/docker-projects/test-vpn/data`
- Percorso dati nel container: `/var/lib/app/data`

Il budget disco è una prenotazione gestionale del portale, non una quota fisica ext4.
Non impedisce al container di scrivere oltre il valore selezionato. Le immagini e i layer Docker
sono conservati nel Docker Root Dir configurato sul server.

## Rete

Nessuna porta pubblicata dal compose.

OpenSSH Server, se installato, non viene avviato automaticamente. Configurare utenti,
autenticazione e pubblicazione della porta prima di abilitarlo.
