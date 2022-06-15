---
title: Modifications dans Access (référence de base de données de bureau Access)
TOCTitle: Changes in Access
description: Access ne prend pas en charge les projets de données Access (ADP). Access introduit un nouveau type d'application qui vous permet de créer des applications web Access.
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 91e13bbcf10cf36866842c90b6062ee6bc7f6374
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083814"
---
# <a name="changes-in-access"></a>Modifications apportées dans Access

**S’applique à :** Access 2013, Office 2013

Access ne prend pas en charge les projets de données Access (ADP). Access introduit un nouveau type d'application qui vous permet de créer des applications web Access. Ce nouveau type vous permet de créer des applications web qui utilisent la puissance de SQL Server sur site ou dans le cloud.

Dans une application Access sur SharePoint Server, lorsque vous créez un tableau, une requête ou une macro de données dans le client Access dans lequel vous créez des tableaux, des vues ou des déclencheurs dans une base de données SQL Server, vous pouvez ouvrir votre base de données dans d'autres applications qui se connectent à SQL Server à l'aide du client Access. Cette option vous permet de partager des données ou de charger des données à partir d'autres systèmes dans votre application Access.

Avec Office 365 et Access, vous pouvez créer des applications directement pour les utilisateurs sans avoir à vous soucier des défis de déploiement, des problèmes d'installation de logiciels ou de la compatibilité avec le système d'exploitation. Créez votre application à un emplacement et partagez-la sur le web avec la puissance de SQL Azure et de SQL Server.

[SQL Azure](/azure/azure-sql/database/sql-database-paas-overview), la version cloud de SQL Server, ne gère pas les fonctionnalités desquelles dépendent les projets de données Access (ADP) pour fonctionner. Pour prendre en charge les fichiers ADP sur SQL Azure, Access nécessite des modifications importantes.

Pour ces raisons, Access ne prend pas en charge les ADPs. Les projets ADP sont très utiles pour SQL Server dans un environnement sur site, mais de grands changements ont eu lieu depuis qu'ils ont été introduits dans Access 2000. Désormais, les utilisateurs veulent que leur base de données soit accessible partout.

## <a name="adp-support-and-the-future"></a>Prise en charge des projets ADP et perspectives pour la suite

Les projets ADP fonctionnent toujours dans les versions antérieures d'Access. Vous pouvez continuer à développer vos applications ADP et nous continuerons à prendre en charge les versions antérieures d'Access dans le cadre de la [politique de support](https://support.microsoft.com/lifecycle/search). Nous ne mettrons pas à jour les versions plus anciennes d'Access pour prendre en charge les nouvelles versions de SQL Server ou de SQL Azure. Par conséquent, vous pouvez rencontrer des problèmes si vous utilisez SQL Server 2012 ou des versions ultérieures avec votre projet de données Access (ADP). Les projets ADP continueront à prendre en charge SQL 2008 R2 et les versions antérieures.

Pour la suite, les développeurs de projets ADP peuvent envisager différentes possibilités :

- **Procéder à une conversion en une application Access**: à l'aide d'Access, vous pouvez importer vos tableaux dans une nouvelle application Access et les formulaires de votre application sont automatiquement créés pour vous. Vous pouvez étendre les fonctionnalités des formulaires de base qu'Access crée pour vous et les utilisateurs peuvent utiliser votre application sur le web. Bien que certaines des fonctionnalités que vous utilisez dans les projets ADP puissent ne pas être disponibles pour l'instant, Microsoft va continuer à apporter des améliorations à son produit pour ce type d'application.

- **Procéder à une conversion en une base de données de bureau liée**: Access prend toujours en charge la création de bases de données de bureau au format .accdb. Vous pouvez convertir votre application au format .accdb, avec l'ensemble de vos formulaires et états existants, et laisser les données dans SQL Server. Vous pouvez créer une liaison avec la base de données SQL Server à l'aide de tableaux liés et votre application continuera à fonctionner avec les mêmes données.

- **Créer une application hybride**: si votre application est volumineuse et que vous ne voulez pas convertir tout le contenu en même temps, vous pouvez importer vos données dans une application Access et créer une liaison avec la base de données SQL Server à partir d'un fichier .accdb. Cela permet de migrer progressivement, d'ajouter des formulaires et des fonctionnalités au fil du temps à votre application Access tout en conservant votre application cliente en tant que fichier .accdb avec des tableaux liés à la base de données SQL Server sous-jacente de l'application Access.

- **Procéder à une mise niveau vers .NET Framework**: si votre application est complexe, vous pouvez envisager de passer à une plateforme de développement professionnel, comme .NET Framework. SQL Server est conçu pour faciliter l'utilisation de votre infrastructure de base de données existante que vous avez déjà créée et le développement des fonctionnalités de votre application, sans avoir à réécrire la quasi-intégralité de votre code.

## <a name="conclusion"></a>Conclusion

Access est conçu pour connecter les bases de données au nuage grâce aux technologies SharePoint Server et SQL Server, ainsi que pour utiliser facilement Office 365. Access est conçu pour vous aider à créer et partager rapidement des applications métier reposant sur les données afin de contribuer à la gestion de votre activité.

## <a name="see-also"></a>Voir aussi

- [Nouveautés d’Access 2013 pour les développeurs](/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)
