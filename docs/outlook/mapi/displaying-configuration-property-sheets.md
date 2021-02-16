---
title: Affichage des feuilles de propriétés de configuration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421311"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="9d12b-103">Affichage des feuilles de propriétés de configuration</span><span class="sxs-lookup"><span data-stu-id="9d12b-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="9d12b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d12b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d12b-105">Les fournisseurs de transport utilisent la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) pour implémenter des feuilles de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d12b-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="9d12b-106">Lors de **l’appel de DoConfigPropSheet,** le fournisseur de transport transmet un pointeur vers un tableau de propriétés, ainsi que des informations sur leur affichage.</span><span class="sxs-lookup"><span data-stu-id="9d12b-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="9d12b-107">MAPI présente ensuite les propriétés à l’utilisateur au moyen d’une boîte de dialogue standard.</span><span class="sxs-lookup"><span data-stu-id="9d12b-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="9d12b-108">Nous vous encourageons vivement à utiliser ce mécanisme de feuille de propriétés lors de l’implémentation de votre fournisseur de transport en raison de l’avantage pour l’utilisateur d’une interface cohérente.</span><span class="sxs-lookup"><span data-stu-id="9d12b-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="9d12b-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="9d12b-109">Transport providers</span></span>

<span data-ttu-id="9d12b-110">Les fournisseurs de transport peuvent utiliser la [fonction BuildDisplayTable](builddisplaytable.md) pour simplifier la construction d’un tableau d’affichage à utiliser avec **DoConfigPropSheet.**</span><span class="sxs-lookup"><span data-stu-id="9d12b-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="9d12b-111">Les fournisseurs de transport peuvent également utiliser directement l’API de feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9d12b-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="9d12b-112">Pour mettre en mémoire tampon les modifications apportées aux propriétés, les fournisseurs de transport peuvent utiliser [la fonction CreateIProp.](createiprop.md)</span><span class="sxs-lookup"><span data-stu-id="9d12b-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="9d12b-113">Cela simplifie la gestion des annulations par l’utilisateur, tandis que l’utilisateur modifie les valeurs stockées dans les propriétés.</span><span class="sxs-lookup"><span data-stu-id="9d12b-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="9d12b-114">Si nécessaire, un fournisseur de transport peut également fournir une boîte de dialogue d’Assistant pour simplifier les tâches de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d12b-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

