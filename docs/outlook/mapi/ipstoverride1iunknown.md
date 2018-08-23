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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e73115811fe0009769826e0f6a011c489772f770
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569847"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="fee6d-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fee6d-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="fee6d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fee6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fee6d-105">Permet à un fournisseur de magasin de fichier (.pst) de dossiers personnels substituer la stratégie PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="fee6d-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fee6d-106">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="fee6d-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="fee6d-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="fee6d-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="fee6d-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fee6d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fee6d-109">Fournisseur de banque PST</span><span class="sxs-lookup"><span data-stu-id="fee6d-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="fee6d-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="fee6d-110">Called by:</span></span>  <br/> |<span data-ttu-id="fee6d-111">Client</span><span class="sxs-lookup"><span data-stu-id="fee6d-111">Client</span></span>  <br/> |
|<span data-ttu-id="fee6d-112">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="fee6d-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fee6d-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="fee6d-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fee6d-114">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="fee6d-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fee6d-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="fee6d-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="fee6d-116">Récupère la liste des enregistrements pour le fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="fee6d-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="fee6d-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="fee6d-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="fee6d-118">Enregistre les fichiers de dossiers personnels pour le déverrouillage automatique, en évitant les autres appels à HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="fee6d-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="fee6d-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="fee6d-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="fee6d-120">Déverrouille le fichier de dossiers personnels de la croissance.</span><span class="sxs-lookup"><span data-stu-id="fee6d-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fee6d-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="fee6d-121">Remarks</span></span>

<span data-ttu-id="fee6d-122">Les identificateurs d’Interface Gestionnaire remplacer PST pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous serez les trouver dans la rubrique [Constantes MAPI](mapi-constants.md) et peuvent copier et les ajouter à votre code.</span><span class="sxs-lookup"><span data-stu-id="fee6d-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="fee6d-123">Pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fee6d-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="fee6d-124">Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="fee6d-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fee6d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fee6d-125">See also</span></span>



[<span data-ttu-id="fee6d-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fee6d-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

