---
title: Propriété canonique PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398072"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="a3862-103">Propriété canonique PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="a3862-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="a3862-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3862-105">Contient un objet attachment généralement accédé via l’interface Object Linking and Embedding (OLE) **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="a3862-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3862-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a3862-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3862-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="a3862-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="a3862-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a3862-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3862-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="a3862-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="a3862-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a3862-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3862-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a3862-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a3862-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a3862-112">Area:</span></span>  <br/> |<span data-ttu-id="a3862-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="a3862-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3862-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3862-114">Remarks</span></span>

<span data-ttu-id="a3862-115">Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="a3862-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="a3862-116">Le type d’encodage OLE peut être déterminée à partir de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3862-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="a3862-117">Pour une pièce jointe associée à la valeur **ATTACH_EMBEDDED_MSG** , l’interface de [IMessage:IMAPIProp](imessageimapiprop.md) peut être utilisée pour un accès rapide.</span><span class="sxs-lookup"><span data-stu-id="a3862-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="a3862-118">Pour un objet OLE incorporé dynamique, la propriété **PR_ATTACH_DATA_OBJ** contient ses propres informations de rendu et la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) doit être inexistant ou vide.</span><span class="sxs-lookup"><span data-stu-id="a3862-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="a3862-119">Pour une pièce jointe au document OLE, le fournisseur de banque de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="a3862-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="a3862-120">Les propriétés **PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété.</span><span class="sxs-lookup"><span data-stu-id="a3862-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="a3862-121">Pour un objet de stockage, tel qu’un fichier composé OLE 2.0 au format d’un document, certains fournisseurs de services pouvoir être ouvert avec l’interface MAPI **IStreamDocfile** , une sous-classe de **IStream** sans membres supplémentaires, conçu pour optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="a3862-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="a3862-122">L’enregistrement potentiel est suffisant pour justifier la tentative d’ouverture de **PR_ATTACH_DATA_OBJ** via **IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="a3862-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="a3862-123">Si **MAPI_E_INTERFACE_NOT_SUPPORTED** est renvoyée, le client peut ensuite ouvrir **PR_ATTACH_DATA_BIN** avec **IStream**.</span><span class="sxs-lookup"><span data-stu-id="a3862-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="a3862-124">Si l’application cliente ou un fournisseur de services ne peuvent pas ouvrir un sous-objet de pièce jointe à l’aide de **PR_ATTACH_DATA_OBJ** à l’aide de **PR_ATTACH_METHOD**, elle doit utiliser **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="a3862-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="a3862-125">Pour plus d’informations sur les formats et les interfaces OLE, consultez [OLE et transfert de données](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3862-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a3862-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a3862-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3862-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a3862-127">Protocol specifications</span></span>

<span data-ttu-id="a3862-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3862-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3862-129">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="a3862-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="a3862-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a3862-130">Header Files</span></span>

<span data-ttu-id="a3862-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3862-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3862-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a3862-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3862-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a3862-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a3862-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="a3862-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3862-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3862-135">See also</span></span>



[<span data-ttu-id="a3862-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a3862-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3862-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a3862-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3862-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a3862-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3862-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a3862-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

