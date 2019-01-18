---
title: Fournisseurs de services et composants
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717243"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="88f76-102">Fournisseurs de services et composants</span><span class="sxs-lookup"><span data-stu-id="88f76-102">Service providers and components</span></span>


<span data-ttu-id="88f76-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88f76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88f76-104">Les fournisseurs de services sont des composants qui étendent les fonctionnalités des fournisseurs de données par l'implémentation d'interfaces qui ne sont pas prises en charge en mode natif par le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="88f76-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="88f76-105">Microsoft Data Access offre une *architecture de composant* qui permet à des composants individuels spécialisés d’implémenter discrètes définit des fonctionnalités de base de données ou « services », sur des magasins plus limitées.</span><span class="sxs-lookup"><span data-stu-id="88f76-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="88f76-106">Par conséquent, au lieu de magasins de données à fournir sa propre implémentation des fonctionnalités étendues ou de forcer les applications génériques pour implémenter les fonctionnalités de base de données en interne, composants du service de fournissent une implémentation courante que n’importe quelle application utiliser pour accéder à n’importe quel magasin de données.</span><span class="sxs-lookup"><span data-stu-id="88f76-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="88f76-107">Le fait que certaines fonctionnalités implémentée en mode natif par le magasin de données et d’autres par le biais de composants génériques est transparent pour l’application.</span><span class="sxs-lookup"><span data-stu-id="88f76-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="88f76-p102">Par exemple, un moteur de curseur tel que le service de curseur Microsoft pour OLE DB, est un composant de service qui peut utiliser des données provenant d'un magasin de données séquentiel, de type avant uniquement, pour produire des données qu'il est possible de faire défiler. Les autres fournisseurs de services généralement utilisés par ADO sont le fournisseur de persistance Microsoft OLE DB (pour l'enregistrement de données dans un fichier), le service de mise en forme des données Microsoft pour OLE DB (pour les **jeux d'enregistrements** hiérarchiques) et le fournisseur d'accès à distance Microsoft OLE DB (pour l'appel des fournisseurs de données sur un ordinateur distant).</span><span class="sxs-lookup"><span data-stu-id="88f76-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="88f76-110">Pour plus d'informations sur les fournisseurs de services et de données, consultez l'[annexe A : Fournisseurs](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="88f76-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

