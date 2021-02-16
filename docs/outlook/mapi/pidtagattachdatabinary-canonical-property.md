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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356545"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="75acf-103">Propriété canonique PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="75acf-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="75acf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75acf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75acf-105">Contient des données de pièces jointes binaires généralement accessibles via l’interface **IStream** OLE (Object Linking and Embedding).</span><span class="sxs-lookup"><span data-stu-id="75acf-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75acf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="75acf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75acf-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="75acf-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="75acf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="75acf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75acf-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="75acf-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="75acf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="75acf-110">Data type:</span></span>  <br/> |<span data-ttu-id="75acf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75acf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="75acf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="75acf-112">Area:</span></span>  <br/> |<span data-ttu-id="75acf-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="75acf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75acf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="75acf-114">Remarks</span></span>

<span data-ttu-id="75acf-115">Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est ATTACH_BY_VALUE, qui est la méthode de pièce jointe habituelle et la seule à être prise en charge.</span><span class="sxs-lookup"><span data-stu-id="75acf-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="75acf-116">**PR_ATTACH_DATA_BIN** contient également une pièce jointe OLE 1.0 **OLESTREAM** lorsque la valeur de PR_ATTACH_METHOD **est** ATTACH_OLE.</span><span class="sxs-lookup"><span data-stu-id="75acf-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="75acf-117">**Les pièces jointes OLESTREAM** peuvent être copiées dans un fichier en appelant la méthode OLE **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="75acf-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="75acf-118">Le type de codage OLE peut être déterminé à partir de **la propriété PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="75acf-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="75acf-119">Pour une pièce jointe de document OLE, le fournisseur de magasin de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="75acf-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="75acf-120">Notez **que PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété.</span><span class="sxs-lookup"><span data-stu-id="75acf-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="75acf-121">Pour un objet de stockage, tel qu’un fichier composé au format docfile OLE 2.0, certains fournisseurs de services lui permettent d’être ouvert avec l’interface MAPI **IStreamDocfile** pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="75acf-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="75acf-122">Un fournisseur qui prend **en charge IStreamDocfile** doit l’exposer sur **PR_ATTACH_DATA_OBJ** et peut éventuellement l’exposer **sur PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="75acf-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="75acf-123">Pour plus d’informations sur les interfaces et les formats OLE, voir [OLE et Transfert de données.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="75acf-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75acf-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="75acf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75acf-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="75acf-125">Protocol specifications</span></span>

<span data-ttu-id="75acf-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75acf-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75acf-127">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="75acf-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="75acf-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="75acf-128">Header Files</span></span>

<span data-ttu-id="75acf-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75acf-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="75acf-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="75acf-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="75acf-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75acf-131">Mapitags.h</span></span>
  
> <span data-ttu-id="75acf-132">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="75acf-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75acf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75acf-133">See also</span></span>



[<span data-ttu-id="75acf-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="75acf-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75acf-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="75acf-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75acf-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="75acf-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75acf-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="75acf-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

