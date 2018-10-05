---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389105"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="c1b0d-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1b0d-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="c1b0d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1b0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1b0d-105">Fournisseur de magasin de ressources d’accès d’un fichier de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="c1b0d-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1b0d-106">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="c1b0d-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="c1b0d-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1b0d-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="c1b0d-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c1b0d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1b0d-109">Fournisseur de banque PST</span><span class="sxs-lookup"><span data-stu-id="c1b0d-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="c1b0d-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c1b0d-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1b0d-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="c1b0d-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="c1b0d-112">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="c1b0d-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c1b0d-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="c1b0d-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c1b0d-114">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="c1b0d-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c1b0d-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="c1b0d-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="c1b0d-116">Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="c1b0d-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1b0d-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1b0d-117">Remarks</span></span>

<span data-ttu-id="c1b0d-118">Les identificateurs d’Interface Gestionnaire remplacer PST pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous serez les trouver dans la rubrique [Constantes MAPI](mapi-constants.md) et peuvent copier et les ajouter à votre code.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="c1b0d-119">Pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="c1b0d-120">Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="c1b0d-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1b0d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b0d-121">See also</span></span>



[<span data-ttu-id="c1b0d-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1b0d-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

