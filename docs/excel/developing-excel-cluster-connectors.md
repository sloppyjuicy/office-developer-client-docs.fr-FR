---
title: Développement de connecteurs de Cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782009"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="b2993-103">Développement de connecteurs de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="b2993-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="b2993-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b2993-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b2993-105">Connecteurs de cluster Excel fournissent un moyen de déchargement automatiquement les appels de fonction définie par l’utilisateur de sécurisées pour le cluster dans une solution XLL un serveur en cluster.</span><span class="sxs-lookup"><span data-stu-id="b2993-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="b2993-106">Pour obtenir une description des fonctions définies par l’utilisateur de cluster sécurisé, voir [Fonctions sécurisées pour le Cluster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b2993-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="b2993-107">Cette déchargement peut améliorer les performances en activant la plus de ressources informatiques à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b2993-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="b2993-108">Un connecteur de cluster est généralement développé par un fournisseur de cluster de calcul hautes performances.</span><span class="sxs-lookup"><span data-stu-id="b2993-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="b2993-109">Connecteurs de cluster</span><span class="sxs-lookup"><span data-stu-id="b2993-109">Cluster Connectors</span></span>

<span data-ttu-id="b2993-110">Un connecteur de cluster est une DLL qui fournit des points d’entrée définis que Microsoft Excel utilise pour coordonner les appels de fonction définie par l’utilisateur de sécurisées pour le cluster.</span><span class="sxs-lookup"><span data-stu-id="b2993-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="b2993-111">Il sert d’interface entre Excel et le cluster de calcul hautes performances, pour la session de gestion, permettant de fonction appelle (en passant le nom complet de fonction et les arguments réels de l’appel) et pour retourner les résultats de l’appel vers Excel via un mécanisme de rappel.</span><span class="sxs-lookup"><span data-stu-id="b2993-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="b2993-112">Pour créer un connecteur de cluster, créez une DLL qui expose les points d’entrée répertoriés dans les [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b2993-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="b2993-113">Installation d’un connecteur de Cluster</span><span class="sxs-lookup"><span data-stu-id="b2993-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="b2993-114">Pour rendre un connecteur de cluster disponibles dans Excel, le code du programme d’installation du connecteur doit installer la DLL du connecteur sur l’ordinateur sur lequel Excel est installé.</span><span class="sxs-lookup"><span data-stu-id="b2993-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="b2993-115">En outre, le code du programme d’installation du connecteur doit ajouter une entrée pour le connecteur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="b2993-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="b2993-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span><span class="sxs-lookup"><span data-stu-id="b2993-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="b2993-117">Ajouter un nœud à cette clé pour le connecteur de cluster qui spécifie les chaînes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2993-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="b2993-118">`Name`— le nom qui apparaîtra dans la liste des connecteurs de cluster dans Excel.</span><span class="sxs-lookup"><span data-stu-id="b2993-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="b2993-119">`Filename`— le chemin d’accès complet de la DLL.</span><span class="sxs-lookup"><span data-stu-id="b2993-119">`Filename`—the full path for the DLL.</span></span>
    

