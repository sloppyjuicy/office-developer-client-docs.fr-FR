---
title: Développement de connecteurs de cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412596"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="c0c83-103">Développement de connecteurs de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="c0c83-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="c0c83-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0c83-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0c83-105">Les connecteurs de cluster Excel permettent de décharger automatiquement les appels de fonctions définies par l’utilisateur sécurisés par un cluster dans une XLL vers un serveur en cluster.</span><span class="sxs-lookup"><span data-stu-id="c0c83-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="c0c83-106">Pour obtenir une description des fonctions définies par l’utilisateur sécurisées pour le cluster, voir [Fonctions sécurisées de cluster.](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="c0c83-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="c0c83-107">Ce déchargement peut améliorer les performances en permettant d’utiliser davantage de ressources informatiques.</span><span class="sxs-lookup"><span data-stu-id="c0c83-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="c0c83-108">Un connecteur de cluster est généralement développé par un fournisseur de cluster de calcul hautes performances.</span><span class="sxs-lookup"><span data-stu-id="c0c83-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="c0c83-109">Connecteurs de cluster</span><span class="sxs-lookup"><span data-stu-id="c0c83-109">Cluster Connectors</span></span>

<span data-ttu-id="c0c83-110">Un connecteur de cluster est une DLL qui fournit des points d’entrée définis qu’Excel utilise pour coordonner les appels de fonctions définies par l’utilisateur sécurisés du cluster.</span><span class="sxs-lookup"><span data-stu-id="c0c83-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="c0c83-111">Il sert d’interface entre Excel et le cluster de calcul hautes performances, pour la gestion des sessions, pour effectuer des appels de fonction (en passant le nom complet de la fonction et les arguments réels de l’appel) et pour renvoyer les résultats des appels à Excel via un mécanisme de rappel.</span><span class="sxs-lookup"><span data-stu-id="c0c83-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="c0c83-112">Pour créer un connecteur de cluster, créez une DLL qui expose les points d’entrée répertoriés dans les fonctions du [connecteur de cluster Excel.](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="c0c83-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="c0c83-113">Installation d’un connecteur de cluster</span><span class="sxs-lookup"><span data-stu-id="c0c83-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="c0c83-114">Pour rendre un connecteur de cluster disponible dans Excel, le code d’installation du connecteur doit installer la DLL du connecteur sur l’ordinateur sur lequel Excel est installé.</span><span class="sxs-lookup"><span data-stu-id="c0c83-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="c0c83-115">En outre, le code d’installation du connecteur doit ajouter une entrée pour le connecteur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c83-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="c0c83-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="c0c83-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span></span>\
  
<span data-ttu-id="c0c83-117">Ajoutez un nœud à cette clé pour le connecteur de cluster qui spécifie les chaînes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0c83-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="c0c83-118">`Name`—nom qui apparaîtra dans la liste des connecteurs de cluster dans Excel.</span><span class="sxs-lookup"><span data-stu-id="c0c83-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="c0c83-119">`Filename`—chemin d’accès complet de la DLL.</span><span class="sxs-lookup"><span data-stu-id="c0c83-119">`Filename`—the full path for the DLL.</span></span>
    

