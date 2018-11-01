---
title: Modifications apportées dans Access (référence de base de données du bureau Access)
TOCTitle: Changes in Access
description: Access ne prend pas en charge les projets de données Access (ADP). Access introduit un nouveau type d'application qui vous permet de créer des applications web Access.
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 4563ccafb9f4078f7016abf6d5bb96ac37b4bddd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878800"
---
# <a name="changes-in-access"></a>Modifications apportées dans Access

**S’applique à :** Access 2013 | Office 2013

Access ne prend pas en charge les projets de données Access (ADP). Access introduit un nouveau type d'application qui vous permet de créer des applications web Access. À l’aide de ce type d’application, vous pouvez créer des applications web qui utilisent la puissance de SQL Server sur site ou dans le cloud.

Dans une application Access dans SharePoint Server, lorsque vous créez une table, une requête ou une macro de données dans le client d’accès dans lequel vous créez tables, vues ou déclencheurs dans une base de données SQL Server, en utilisant le client Access, vous pouvez ouvrir votre base de données à d’autres applications qui conn type de contenu externe à SQL Server. Cela vous permet de partager vos données ou de charger des données à partir d’autres systèmes utilisés dans votre application Access.

Avec Office 365 et Access, vous pouvez créer des applications directement pour les utilisateurs sans avoir à vous soucier des défis de déploiement, des problèmes d'installation de logiciels ou de la compatibilité avec le système d'exploitation. Créez votre application à un emplacement et partagez-la sur le web avec la puissance de SQL Azure et de SQL Server.

[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), la version cloud de SQL Server, ne gère pas les fonctionnalités desquelles dépendent les projets de données Access (ADP) pour fonctionner. Pour prendre en charge les fichiers ADP sur SQL Azure, Access nécessite des modifications importantes.

C'est pour cela qu'Access ne prend pas en charge les projets ADP. ADP ont été un excellent outil pour l’utilisation de SQL Server dans un environnement local ; Toutefois, la plupart a été modifié depuis ADP ont été introduites dans Access 2000. Désormais, les utilisateurs veulent que leur base de données soit accessible partout.

## <a name="adp-support-and-the-future"></a>Prise en charge des projets ADP et perspectives pour la suite

Les projets ADP fonctionnent toujours dans les versions antérieures d'Access. Vous pouvez continuer à développer vos applications ADP et nous continuerons à prendre en charge les versions antérieures d'Access dans le cadre de la [politique de support](https://support.microsoft.com/lifecycle/search). Nous ne mettrons pas à jour les versions plus anciennes d'Access pour prendre en charge les nouvelles versions de SQL Server ou de SQL Azure. Par conséquent, vous pouvez rencontrer des problèmes si vous utilisez SQL Server 2012 ou des versions ultérieures avec votre projet de données Access (ADP). Les projets ADP continueront à prendre en charge SQL 2008 R2 et les versions antérieures.

Pour la suite, les développeurs de projets ADP peuvent envisager différentes possibilités :

- **Convertir une application Access** – à l’aide de l’accès, vous pouvez importer des tables dans une application Access, et des formulaires pour votre application sont créés automatiquement pour vous. Vous pouvez étendre les fonctionnalités des formes de base que Microsoft Access crée pour vous, et les utilisateurs peuvent utiliser votre application sur le web. Bien que certaines des fonctionnalités que vous utilisez dans les projets ADP puissent ne pas être disponibles pour l'instant, Microsoft va continuer à apporter des améliorations à son produit pour ce type d'application.

- **Convertir une base de données du bureau liée** – Access Server continue de prendre en charge la création de bases de données du bureau dans le format de fichier .accdb. Vous pouvez convertir votre application au format .accdb, avec l'ensemble de vos formulaires et états existants, et laisser les données dans SQL Server. Vous pouvez lier à la base de données SQL Server à l’aide de tables liées et votre application continuera de fonctionner sur les mêmes données.

- **Créer une application hybride** – si votre application est importante et vous ne voulez pas convertir tout en même temps, vous pouvez importer des données dans une application Access et le lier à la base de données SQL Server à partir d’un .accdb. Cela permet de que migrer graduellement, ajout de formulaires et les fonctionnalités au fil du temps à votre application Access, tout en conservant votre application cliente comme un .accdb avec les tables liées à la base de données SQL Server derrière l’application Access.

- **Mise à niveau vers le .NET Framework** , votre application peut être assez complexe à prendre en compte le déplacement vers une plateforme de développement professionnel tel que le .NET Framework. SQL Server est conçu pour faciliter l’accès vous permettent d’utiliser votre infrastructure de base de données existante et étendre les fonctionnalités de votre application sans avoir à réécrire considérablement votre code.

## <a name="conclusion"></a>Conclusion

Access est conçu pour connecter les bases de données au nuage grâce aux technologies SharePoint Server et SQL Server, ainsi que pour utiliser facilement Office 365. Access est conçu pour vous aider à créer et partager rapidement des applications métier reposant sur les données afin de contribuer à la gestion de votre activité.

## <a name="see-also"></a>Voir aussi

- [Nouveautés pour les développeurs Access 2013](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


