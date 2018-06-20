---
title: Affichage des feuilles de propriétés de configuration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: aa3ddecbd5af56eef16f5ae3a349a027e689fc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783185"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="368b2-103">Affichage des feuilles de propriétés de configuration</span><span class="sxs-lookup"><span data-stu-id="368b2-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="368b2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="368b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="368b2-105">Fournisseurs de transport utilisent la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) pour implémenter des feuilles de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="368b2-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="368b2-106">Lors de l’appel **DoConfigPropSheet**, le fournisseur de transport transmet un pointeur vers un tableau de propriétés ainsi que des informations sur la façon de les afficher.</span><span class="sxs-lookup"><span data-stu-id="368b2-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="368b2-107">Ensuite, MAPI présente les propriétés à l’utilisateur au moyen d’une boîte de dialogue standard.</span><span class="sxs-lookup"><span data-stu-id="368b2-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="368b2-108">Il est vivement recommandé d’utiliser ce mécanisme de feuille de propriété lors de l’implémentation de votre fournisseur de transport en raison de l’avantage pour l’utilisateur d’une interface cohérente.</span><span class="sxs-lookup"><span data-stu-id="368b2-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="368b2-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="368b2-109">Transport providers</span></span>

<span data-ttu-id="368b2-110">Fournisseurs de transport peuvent utiliser la fonction [BuildDisplayTable](builddisplaytable.md) pour simplifier la construction d’un tableau d’affichage pour une utilisation avec **DoConfigPropSheet**.</span><span class="sxs-lookup"><span data-stu-id="368b2-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="368b2-111">Fournisseurs de transport peuvent également utiliser l’API de feuille de propriété directement.</span><span class="sxs-lookup"><span data-stu-id="368b2-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="368b2-112">Modifications apportées aux propriétés de la mémoire tampon, fournisseurs de transport peut utiliser la fonction [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="368b2-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="368b2-113">Cela simplifie la gestion des annulations par l’utilisateur pendant que l’utilisateur modifie les valeurs stockées dans les propriétés.</span><span class="sxs-lookup"><span data-stu-id="368b2-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="368b2-114">Si nécessaire, un fournisseur de transport peut également fournir une boîte de dialogue Assistant case pour simplifier les tâches de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="368b2-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

