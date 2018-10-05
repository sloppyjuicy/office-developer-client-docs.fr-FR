---
title: Propriété canonique PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396882"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="22f4f-103">Propriété canonique PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="22f4f-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="22f4f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22f4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22f4f-105">Contient le nom d’affichage d’un destinataire dans un formulaire sécurisé qui ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="22f4f-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22f4f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="22f4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22f4f-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="22f4f-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="22f4f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="22f4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22f4f-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="22f4f-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="22f4f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="22f4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="22f4f-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="22f4f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="22f4f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="22f4f-112">Area:</span></span>  <br/> |<span data-ttu-id="22f4f-113">Address</span><span class="sxs-lookup"><span data-stu-id="22f4f-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22f4f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="22f4f-114">Remarks</span></span>

<span data-ttu-id="22f4f-115">Ces propriétés doivent être implémentées par tous les fournisseurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="22f4f-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="22f4f-116">Elles contiennent la version du nom complet du destinataire est transmise avec le message.</span><span class="sxs-lookup"><span data-stu-id="22f4f-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="22f4f-117">Pour la plupart des fournisseurs de carnet d’adresses, ces propriétés ont la même valeur que la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22f4f-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="22f4f-118">Fournisseurs qui n’ont pas un nom d’affichage d’informations sécurisé renvoyer des modifications PT_ERROR et MAPI le nom complet en ajoutant le nom entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="22f4f-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="22f4f-119">Une application cliente peut utiliser cette propriété pour éviter toute altération ou « usurpation d’identité » des entrées.</span><span class="sxs-lookup"><span data-stu-id="22f4f-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="22f4f-120">Un exemple d’usurpation transmet John Doe comme pré (qu’un expert).</span><span class="sxs-lookup"><span data-stu-id="22f4f-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22f4f-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="22f4f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22f4f-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="22f4f-122">Protocol specifications</span></span>

<span data-ttu-id="22f4f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f4f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f4f-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="22f4f-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22f4f-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f4f-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f4f-126">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="22f4f-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="22f4f-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f4f-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f4f-128">Gère les communications d’un client avec un serveur NSPI Name Service Provider Interface ().</span><span class="sxs-lookup"><span data-stu-id="22f4f-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="22f4f-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f4f-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f4f-130">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="22f4f-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="22f4f-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f4f-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f4f-132">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="22f4f-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22f4f-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="22f4f-133">Header files</span></span>

<span data-ttu-id="22f4f-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22f4f-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="22f4f-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="22f4f-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="22f4f-136">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="22f4f-136">Mapitags.h</span></span>
  
> <span data-ttu-id="22f4f-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="22f4f-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22f4f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22f4f-138">See also</span></span>



[<span data-ttu-id="22f4f-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="22f4f-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22f4f-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="22f4f-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22f4f-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="22f4f-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22f4f-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="22f4f-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

