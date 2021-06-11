---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315497"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="a228c-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a228c-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="a228c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a228c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a228c-105">Permet à un fournisseur de magasins de dossiers personnels (PST) de remplacer la stratégie PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="a228c-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a228c-106">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="a228c-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="a228c-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="a228c-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="a228c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a228c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a228c-109">Fournisseur de magasins PST</span><span class="sxs-lookup"><span data-stu-id="a228c-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="a228c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a228c-110">Called by:</span></span>  <br/> |<span data-ttu-id="a228c-111">Client</span><span class="sxs-lookup"><span data-stu-id="a228c-111">Client</span></span>  <br/> |
|<span data-ttu-id="a228c-112">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="a228c-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a228c-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="a228c-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a228c-114">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="a228c-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a228c-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="a228c-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="a228c-116">Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="a228c-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="a228c-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="a228c-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="a228c-118">Enregistre les fichiers de dossiers personnels pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="a228c-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="a228c-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="a228c-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="a228c-120">Déverrouille un fichier de dossiers personnels pour la croissance.</span><span class="sxs-lookup"><span data-stu-id="a228c-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a228c-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="a228c-121">Remarks</span></span>

<span data-ttu-id="a228c-122">Les identificateurs d’interface du handler de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) et pourrez les copier et les ajouter à votre code.</span><span class="sxs-lookup"><span data-stu-id="a228c-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="a228c-123">Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="a228c-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="a228c-124">Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="a228c-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a228c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a228c-125">See also</span></span>



[<span data-ttu-id="a228c-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a228c-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

