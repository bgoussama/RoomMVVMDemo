# RoomMVVMDemo

Application Android de gestion de notes locale, construite avec l'architecture MVVM et Room.

## Objectifs pédagogiques

- Comprendre l'architecture MVVM sur Android
- Utiliser Room comme couche de persistance SQLite
- Observer les données avec LiveData
- Afficher une liste performante avec RecyclerView
- Séparer les responsabilités entre Entity, DAO, Repository et ViewModel

## demo video :



https://github.com/user-attachments/assets/3261bd4f-7733-48a5-8189-91e05f32241d



## Architecture
com.example.roommvvmdemo
├── data
│   ├── local
│   │   ├── Note.java          # Entity Room
│   │   ├── NoteDao.java       # Interface d'accès aux données
│   │   └── NoteDatabase.java  # Singleton RoomDatabase
│   └── NoteRepository.java    # Couche intermédiaire données
├── ui
│   ├── MainActivity.java      # Vue principale
│   └── NoteAdapter.java       # Adapter RecyclerView
└── viewmodel
└── NoteViewModel.java     # Logique de présentation

## Fonctionnalités

- Ajouter une note avec titre et description
- Supprimer une note par clic long
- Supprimer toutes les notes
- Persistance locale via Room/SQLite
- Mise à jour automatique de la liste via LiveData
- Survie aux rotations d'écran grâce au ViewModel

## Stack technique

| Composant | Technologie |
|---|---|
| Langage | Java |
| Architecture | MVVM |
| Base de données | Room 2.6.1 |
| Observation | LiveData |
| Liste | RecyclerView 1.4.0 |
| Min SDK | 24 (Android 7.0) |

## Flux de données
MainActivity → NoteViewModel → NoteRepository → NoteDao → Room/SQLite
↑                                                          |
└──────────────── LiveData ←──────────────────────────────┘

## Tests réalisés

- Insertion de notes
- Suppression par clic long
- Suppression globale
- Persistance après fermeture de l'app
- Cohérence des données après rotation d'écran

## Auteur

Oussama Bagy — ENSA Marrakech, GCDSTE 2022–2027
