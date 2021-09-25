---
title: Fournisseurs de services et composants
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0241d5acc866ef69469fedbfb27694ed13e683da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593564"
---
# <a name="service-providers-and-components"></a>Fournisseurs de services et composants


**S’applique à** : Access 2013, Office 2013

Les fournisseurs de services sont des composants qui étendent les fonctionnalités des fournisseurs de données par l'implémentation d'interfaces qui ne sont pas prises en charge en mode natif par le magasin de données.

Microsoft Data Access offre une *architecture de composants* qui permet à des composants individuels spécialisés d'implémenter des ensembles indépendants de fonctionnalités de base de données, appelés services, sur des magasins  disposant de fonctionnalités plus limitées. Ainsi, les magasins de données ne doivent pas mettre en oeuvre des fonctionnalités étendues pas plus que les application génériques ne sont tenues d'implémenter en interne des fonctionnalité de base de données. En effet, les composants de service offrent une implémentation commune que toutes les applications peuvent utiliser pour accéder aux magasins de données. L'implémentation native de certaines fonctionnalités par le magasin de données et l'implémentation d'autres fonctionnalités par l'intermédiaire de composants génériques est transparente pour l'application.

Par exemple, un moteur de curseur tel que le service de curseur Microsoft pour OLE DB, est un composant de service qui peut utiliser des données provenant d'un magasin de données séquentiel, de type avant uniquement, pour produire des données qu'il est possible de faire défiler. Les autres fournisseurs de services généralement utilisés par ADO sont le fournisseur de persistance Microsoft OLE DB (pour l'enregistrement de données dans un fichier), le service de mise en forme des données Microsoft pour OLE DB (pour les **jeux d'enregistrements** hiérarchiques) et le fournisseur d'accès à distance Microsoft OLE DB (pour l'appel des fournisseurs de données sur un ordinateur distant).

Pour plus d’informations sur les fournisseurs de services et de données, consultez l’[annexe A : Fournisseurs](appendix-a-providers.md).

