# astarte_docker_images

Docker images to build/develop `astarte`

## TODO project

astarte-docker/
├── README.md # Documentazione del progetto
├── base-images/ # Dockerfile per immagini base condivise
│ ├── elixir/
│ │ ├── Dockerfile # Immagine base per progetti Elixir
│ │ └── README.md # Documentazione specifica
│ ├── python/
│ │ ├── Dockerfile # Immagine base per progetti Python
│ │ └── README.md
│ └── node/
│ ├── Dockerfile # Immagine base per progetti Node.js
│ └── README.md
├── project-specific/ # Dockerfile specifici per progetti Astarte
│ ├── astarte-housekeeping/
│ │ └── Dockerfile
│ ├── astarte-dashboard/
│ │ └── Dockerfile
│ └── ...
├── utilities/ # Script e utilità per build e testing
│ ├── build.sh # Script per automatizzare il build
│ ├── push.sh # Script per pubblicare le immagini
│ └── cleanup.sh # Script di pulizia delle immagini locali
└── ci/ # Configurazioni CI/CD per immagini
├── github-actions/ # Workflow di GitHub Actions
│ └── build-and-push.yml
└── docker-compose/ # Configurazioni Compose per testing locale
