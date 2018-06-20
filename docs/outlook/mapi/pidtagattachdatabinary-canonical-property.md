---
title: Propriété canonique PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3646f3e3906e62fe148fe1c2b6ddca39013391e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785715"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="2f869-103">Propriété canonique PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="2f869-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="2f869-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2f869-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2f869-105">Contient des données binaires de pièce jointe généralement accédées via l’interface Object Linking and Embedding (OLE) **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2f869-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f869-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2f869-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f869-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="2f869-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="2f869-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2f869-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2f869-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="2f869-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="2f869-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2f869-110">Data type:</span></span>  <br/> |<span data-ttu-id="2f869-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2f869-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2f869-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="2f869-112">Area:</span></span>  <br/> |<span data-ttu-id="2f869-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="2f869-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f869-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f869-114">Remarks</span></span>

<span data-ttu-id="2f869-115">Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est ATTACH_BY_VALUE, qui est le seul doivent être pris en charge et la méthode habituelle de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2f869-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="2f869-116">**PR_ATTACH_DATA_BIN** contient également une pièce jointe OLE 1.0 **OLESTREAM** lorsque la valeur de **PR_ATTACH_METHOD** est ATTACH_OLE.</span><span class="sxs-lookup"><span data-stu-id="2f869-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="2f869-117">Pièces jointes **OLESTREAM** peuvent être copiés dans un fichier en appelant la méthode OLE **IStream::CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="2f869-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="2f869-118">Le type d’encodage OLE peut être déterminée à partir de la propriété **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2f869-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="2f869-119">Pour une pièce jointe au document OLE, le fournisseur de banque de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN **.</span><span class="sxs-lookup"><span data-stu-id="2f869-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="2f869-120">Notez que **PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété.</span><span class="sxs-lookup"><span data-stu-id="2f869-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="2f869-121">Pour un objet de stockage, tel qu’un fichier composé OLE 2.0 au format d’un document, certains fournisseurs de services pouvoir être ouvert avec l’interface MAPI **IStreamDocfile** pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="2f869-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="2f869-122">Un fournisseur qui prend en charge **IStreamDocfile** doit exposer sur **PR_ATTACH_DATA_OBJ** et peut-être éventuellement exposer sur **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="2f869-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="2f869-123">Pour plus d’informations sur les formats et les interfaces OLE, consultez [OLE et transfert de données](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f869-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2f869-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2f869-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f869-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="2f869-125">Protocol specifications</span></span>

<span data-ttu-id="2f869-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f869-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f869-127">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2f869-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="2f869-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2f869-128">Header Files</span></span>

<span data-ttu-id="2f869-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f869-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f869-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2f869-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="2f869-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2f869-131">Mapitags.h</span></span>
  
> <span data-ttu-id="2f869-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="2f869-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f869-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f869-133">See also</span></span>



[<span data-ttu-id="2f869-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2f869-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f869-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2f869-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f869-136">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2f869-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f869-137">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="2f869-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

