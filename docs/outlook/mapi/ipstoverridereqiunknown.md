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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356979"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="16a04-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a04-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="16a04-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16a04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16a04-105">Accède aux ressources d’un fournisseur de magasins de fichiers de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="16a04-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16a04-106">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="16a04-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="16a04-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a04-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="16a04-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="16a04-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="16a04-109">Fournisseur de magasin PST</span><span class="sxs-lookup"><span data-stu-id="16a04-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="16a04-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="16a04-110">Called by:</span></span>  <br/> |<span data-ttu-id="16a04-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="16a04-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="16a04-112">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="16a04-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="16a04-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="16a04-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="16a04-114">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="16a04-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="16a04-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="16a04-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="16a04-116">Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="16a04-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16a04-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="16a04-117">Remarks</span></span>

<span data-ttu-id="16a04-118">Les identificateurs d’interface du handler de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) et pourrez les copier et les ajouter à votre code.</span><span class="sxs-lookup"><span data-stu-id="16a04-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="16a04-119">Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="16a04-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="16a04-120">Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="16a04-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16a04-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a04-121">See also</span></span>



[<span data-ttu-id="16a04-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a04-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

