---
title: Fournisseurs et composants de services
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d215c7c66c489e54d513941604b1c66c0e9094c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881208"
---
# <a name="service-providers-and-components"></a>Fournisseurs et composants de services


**S’applique à**: Access 2013, Office 2013

Les fournisseurs de services sont des composants qui étendent les fonctionnalités des fournisseurs de données par l'implémentation d'interfaces qui ne sont pas prises en charge en mode natif par le magasin de données.

Microsoft Data Access offre une *architecture de composant* qui permet à des composants individuels spécialisés d’implémenter discrètes définit des fonctionnalités de base de données ou « services », sur des magasins plus limitées. Par conséquent, au lieu de magasins de données à fournir sa propre implémentation des fonctionnalités étendues ou de forcer les applications génériques pour implémenter les fonctionnalités de base de données en interne, composants du service de fournissent une implémentation courante que n’importe quelle application utiliser pour accéder à n’importe quel magasin de données. Le fait que certaines fonctionnalités implémentée en mode natif par le magasin de données et d’autres par le biais de composants génériques est transparent pour l’application.

Par exemple, un moteur de curseur tel que le service de curseur Microsoft pour OLE DB, est un composant de service qui peut utiliser des données provenant d'un magasin de données séquentiel, de type avant uniquement, pour produire des données qu'il est possible de faire défiler. Les autres fournisseurs de services généralement utilisés par ADO sont le fournisseur de persistance Microsoft OLE DB (pour l'enregistrement de données dans un fichier), le service de mise en forme des données Microsoft pour OLE DB (pour les **jeux d'enregistrements** hiérarchiques) et le fournisseur d'accès à distance Microsoft OLE DB (pour l'appel des fournisseurs de données sur un ordinateur distant).

Pour plus d'informations sur les fournisseurs de services et de données, consultez l'[annexe A : Fournisseurs](appendix-a-providers.md).

