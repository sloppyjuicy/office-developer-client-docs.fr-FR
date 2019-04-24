---
title: Développement de connecteurs de cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310954"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="d93ea-103">Développement de connecteurs de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="d93ea-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="d93ea-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d93ea-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d93ea-105">Les connecteurs de cluster Excel permettent de décharger automatiquement les appels de fonctions définies par l'utilisateur en cluster dans un XLL sur un serveur en cluster.</span><span class="sxs-lookup"><span data-stu-id="d93ea-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="d93ea-106">Pour obtenir une description des fonctions définies par l'utilisateur en cluster, consultez la rubrique [fonctions de sécurité du cluster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d93ea-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="d93ea-107">Ce délestage peut améliorer les performances en permettant l'utilisation de ressources de calcul supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d93ea-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="d93ea-108">Un connecteur de cluster est généralement développé par un fournisseur de cluster de calcul à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="d93ea-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="d93ea-109">Connecteurs de cluster</span><span class="sxs-lookup"><span data-stu-id="d93ea-109">Cluster Connectors</span></span>

<span data-ttu-id="d93ea-110">Un connecteur de cluster est une DLL qui fournit des points d'entrée définis utilisés par Excel pour coordonner les appels de fonctions définies par l'utilisateur en cluster.</span><span class="sxs-lookup"><span data-stu-id="d93ea-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="d93ea-111">Il sert d'interface entre Excel et le cluster de calcul à hautes performances, pour la gestion des sessions, pour effectuer des appels de fonction (en transmettant le nom de la fonction Complete et les arguments réels de l'appel), et pour renvoyer les résultats de l'appel à Excel via un mécanisme de rappel.</span><span class="sxs-lookup"><span data-stu-id="d93ea-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="d93ea-112">Pour créer un connecteur de cluster, créez une DLL qui expose les points d'entrée figurant dans les [fonctions Excel cluster Connector](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d93ea-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="d93ea-113">Installation d'un connecteur de cluster</span><span class="sxs-lookup"><span data-stu-id="d93ea-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="d93ea-114">Pour qu'un connecteur de cluster soit disponible dans Excel, le code d'installation du connecteur doit installer la DLL du connecteur sur l'ordinateur sur lequel Excel est installé.</span><span class="sxs-lookup"><span data-stu-id="d93ea-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="d93ea-115">En outre, le code d'installation du connecteur doit ajouter une entrée pour le connecteur sous la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="d93ea-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="d93ea-116">Connecteurs de cluster HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel \\</span><span class="sxs-lookup"><span data-stu-id="d93ea-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="d93ea-117">Ajoutez un nœud à cette clé pour le connecteur de cluster qui spécifie les chaînes suivantes:</span><span class="sxs-lookup"><span data-stu-id="d93ea-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="d93ea-118">`Name`: nom qui apparaîtra dans la liste des connecteurs de cluster dans Excel.</span><span class="sxs-lookup"><span data-stu-id="d93ea-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="d93ea-119">`Filename`: chemin d'accès complet de la DLL.</span><span class="sxs-lookup"><span data-stu-id="d93ea-119">`Filename`—the full path for the DLL.</span></span>
    

