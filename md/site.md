# Application Information Document (AID) WSProspect

Version: 0.1  
Date : 12/03/2018  
Status: Draft  
[Version PDF](./site.pdf)  

## Historique des modifications
| Version | Date       | Auteur        | Description de la modification |
|---------|------------|---------------|--------------------------------|
| 0.1     | 12/03/2018 | Bounlay H     | Version initiale               |        

> Note :
Date  : Cette date est la date de fourniture de documents après les  revues.
Des changements cosmétiques peuvent être publiés sans revue. Ceci peut engendrer un changement de date sans modifier le numéro de version.

> Numéro de version : C’est le numéro d'identification de document. Pour la version provisoire, le numéro initial commence par 0.1.  Pour la version de base, le numéro de version commence par 1.0, puis incrémenté par 1 toutes les fois que la révision est passée en revue et validée  par les groupes impactés.

## Auteurs
| Rôle        | Nom           | Société |
|-------------|---------------|---------|
| Developpeur | Bounlay H     | IBM     |

## Révisions
Ce document a été revu par les personnes suivantes :

| Rôle | Nom | Société |
|------|-----|---------|
|      |     |         |

## Approbations
Ce document a été approuvé par les personnes suivantes :

| Rôle | Nom | Société |
|------|-----|---------|
|      |     |         |

## Table des matières

- [Objectifs](./000-index.md#objectifs)
- [Terminologie et Acronymes](./000-index.md#terminologie-et-acronymes)
- [Vue Fonctionnelle](./100-vueFonctionnelle.md)
- [Architecture Technique Général](./200-archiTechnique.md)
- [Bases de Donnees et Dossiers](./300-baseDonnees.md)
- [Interfaces / services](./400-InterfacesServices.md)
- [Batch Jobs](./500-batchJobs.md)
- Interfaces Utilisateurs
- Environnement
- Procedure De Deploiment
- Activites Périodiques
- Procédure De Backup
- Normes Et Conventions
- Historique De L'Application
- Documents De Référence

#	Objectifs

L'objectif du document descriptif d’application (AID) est de fournir aux membres de l'équipe une vue d'ensemble de l'application WS Prospect. L'AID décrit la fonction de l'application, la structure des applications, la configuration de l’application et l'environnement technique. Ce document pourra faire référence à n'importe quelle documentation existante.
L'équipe de delivery tiendra l'AID à jour durant toute la vie de l'application WS Prospect.

# Terminologie et Acronymes
Les acronymes et la terminologie spécifiquement utilisés dans ce document sont décrits ci-dessous.  D'autres acronymes utilisés généralement peuvent être trouvés dans l'ASCP.

| Numéro       |     Terminologie/acronymes	Définition     |        Définition |
| :------------: | :-------------: | :-------------: |
| 1       |     AID     |        Document descriptif d’application |
| 2       |     SME     |        Expert applicatif |

[Table des matières](./999-toc.md) | [Suivant >](./100-vueFonctionnelle.md)
[< Precedent](./000-index.md) | [Table des matières](./999-toc.md) | [Suivant >](./200-archiTechnique.md)

# Vue Fonctionnelle

L’application WS Propsect permet aux utilisateurs de s’inscrire aux formations initiales et continue proposées par L’EMLYON.

##	Diagramme de contexte

![Image](../image/WSProspect-DiagrammeContexte.png)

##	Architecture Fonctionnelle

[< Precedent](./000-index.md) | [Table des matières](./999-toc.md) | [Suivant >](./200-archiTechnique.md)
[< Precedent](./100-vueFonctionnelle.md) | [Table des matières](./999-toc.md) | [Suivant >](./300-baseDonnees.md)

# Architecture Technique Générale

## Architecture applicative

![Image](../plantUML/WSProspect-ArchiApplicative.png)

## Architecture Opérationnel

##	Plateforme Technique

|     Type                           |     OS/Plateforme      |     Logiciel         |     Version        |
|------------------------------------|------------------------|----------------------|--------------------|
|    Serveur Web                     |    Windows             |    IIS               |    7               |
|    Serveur d’application           |    Windows             |    IIS               |    7               |
|    Serveur de base de données      |    Windows Server      |    SQL Server        |    2008            |
|    Serveur FTP                     |    Linux               |    N/A               |    N/A             |
|    Serveur LDAP                    |    Windows             |    N/A               |    N/A             |
|    Langage                         |    C#                  |    .NET              |    4.0             |
|    Outils Développement            |    Windows 7           |    Visual Studio     |    2010 > 2012     |
|    Outils tests                    |                        |                      |                    |
|    SCM (Gestion de code source)    |    Windows             |    GitLab            |                    |
|    Outils Integration Continu      |                        |                      |                    |

##	Authentication et Authorization
L’authentification des appels Web service se fait par jeton, ceux-ci sont générés par Intercom.

##	Gestion d’Erreur
Les erreurs sont gérées par les codes retour HTTP. Il n’y a pas de page d’erreur personnalisée pour l’application.

##	Logging
Les configurations des logs et des rotation log est gérée avec Log4Net.
Le niveau des logs en Production est Info

Ci-dessous  la configuration actuelle :  

##	Caching
N/A (pas d’utilisation de cache pour cette application)

##	Transaction Management
L’application requière un contexte par transaction. Les transactions sont gérées par Entity Framework

##	Autres Eléments Techniques

[< Precedent](./100-vueFonctionnelle.md) | [Table des matières](./999-toc.md) | [Suivant >](./300-baseDonnees.md)
[< Precedent](./200-archiTechnique.md) | [Table des matières](./999-toc.md) | [Suivant >](./xxx.md)

# Base de données

[< Precedent](./200-archiTechnique.md) | [Table des matières](./999-toc.md) | [Suivant >](./xxx.md)
[Index](./000-index.md)

# Table des matières

- [Objectifs](./000-index.md#objectifs)
- [Terminologie et Acronymes](./000-index.md#terminologie-et-acronymes)
- [Vue Fonctionnelle](./100-vueFonctionnelle.md)
- [Architecture Technique Général](./200-archiTechnique.md)
- [Bases de Donnees et Dossiers](./300-baseDonnees.md)
- [Interfaces / services](./400-InterfacesServices.md)
- [Batch Jobs](./500-batchJobs.md)
- Interfaces Utilisateurs
- Environnement
- Procedure De Deploiment
- Activites Périodiques
- Procédure De Backup
- Normes Et Conventions
- Historique De L'Application
- Documents De Référence

[Index](./000-index.md)
