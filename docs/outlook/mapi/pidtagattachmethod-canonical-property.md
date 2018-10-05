---
title: Propriété canonique PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Dernière modification : 07 septembre 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400725"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="b8e3d-103">Propriété canonique PidTagAttachMethod</span><span class="sxs-lookup"><span data-stu-id="b8e3d-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="b8e3d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8e3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8e3d-105">Contient une constante défini par MAPI représentant la façon dont le contenu d’une pièce jointe est accessible.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8e3d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b8e3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8e3d-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="b8e3d-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="b8e3d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b8e3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8e3d-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="b8e3d-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="b8e3d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b8e3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8e3d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8e3d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8e3d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b8e3d-112">Area:</span></span>  <br/> |<span data-ttu-id="b8e3d-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="b8e3d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8e3d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8e3d-114">Remarks</span></span>

<span data-ttu-id="b8e3d-115">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8e3d-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b8e3d-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="b8e3d-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="b8e3d-117">La pièce jointe vient d’être créée.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="b8e3d-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="b8e3d-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="b8e3d-119">La propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contient les données de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="b8e3d-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="b8e3d-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="b8e3d-121">L' **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou la propriété **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contient un chemin d’accès complet qui identifie la pièce jointe aux destinataires d’accéder à un fichier commun serveur.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="b8e3d-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="b8e3d-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="b8e3d-123">La propriété **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contient un chemin d’accès complet qui identifie la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="b8e3d-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="b8e3d-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="b8e3d-125">La propriété **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contient un chemin d’accès complet qui identifie la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="b8e3d-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="b8e3d-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="b8e3d-127">La propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contient un objet incorporé qui prend en charge l’interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="b8e3d-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="b8e3d-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="b8e3d-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="b8e3d-129">La pièce jointe est un objet OLE incorporé.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="b8e3d-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="b8e3d-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="b8e3d-131">Le contenu de pièce jointe n’est pas dans le message.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="b8e3d-132">Une fois créée, tous les objets de pièces jointes ont une valeur initiale **PR_ATTACH_METHOD** **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="b8e3d-133">Fournisseurs de services et les applications clientes sont uniquement requis pour prendre en charge la méthode de pièce jointe représentée par la valeur **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="b8e3d-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="b8e3d-134">Les autres méthodes de pièce jointe sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-134">The other attachment methods are optional.</span></span> <span data-ttu-id="b8e3d-135">La banque de messages n’applique pas la cohérence entre la valeur de **PR_ATTACH_METHOD** et les valeurs d’autres propriétés de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="b8e3d-136">Noms universal naming convention (UNC) sont recommandés pour les chemins complet, qui doivent être utilisées avec **ATTACH_BY_REFERENCE** et **ATTACH_BY_REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="b8e3d-137">Avec **ATTACH_BY_REF_RESOLVE**, un chemin d’accès absolu est plus rapide, car le spouleur MAPI convertit la pièce jointe **ATTACH_BY_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="b8e3d-138">Si **ATTACH_BY_REFERENCE** est défini, **PR_ATTACH_DATA_BIN** doit être vide.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="b8e3d-139">Une passerelle sortante peut activer une pièce jointe **ATTACH_BY_REFERENCE** dans une pièce jointe **ATTACH_BY_VALUE** en copiant des données de pièce jointe dans la propriété **PR_ATTACH_DATA_BIN** .</span><span class="sxs-lookup"><span data-stu-id="b8e3d-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="b8e3d-140">Si **ATTACH_BY_REF_RESOLVE** est défini, **PR_ATTACH_DATA_BIN** doit être vide.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="b8e3d-141">Lorsque le message qui contient la pièce jointe **ATTACH_BY_REF_RESOLVE** est envoyé, le spouleur MAPI copie les données de pièce jointe dans une pièce jointe **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="b8e3d-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="b8e3d-142">Ce processus de résolution place les données de pièce jointe dans **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="b8e3d-143">Si **ATTACH_BY_REF_ONLY** est défini, **PR_ATTACH_DATA_BIN** doit être vide, et le système de messagerie résout jamais la référence de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="b8e3d-144">Utilisez cette valeur lorsque vous souhaitez envoyer le lien, mais pas les données.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="b8e3d-145">Lorsque l’objet OLE est au format OLE 2.0 **IStorage** , les données sont accessibles via **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="b8e3d-146">Lorsque l’objet OLE est au format OLE 1.0 **OLESTREAM** , les données sont accessibles via **PR_ATTACH_DATA_BIN** comme un **IStream**.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="b8e3d-147">Le type du codage OLE peut être déterminé par la valeur **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8e3d-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="b8e3d-148">Pour plus d’informations sur les formats et les interfaces OLE, consultez la *référence du programmeur OLE* .</span><span class="sxs-lookup"><span data-stu-id="b8e3d-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b8e3d-149">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8e3d-149">Remarks</span></span>

<span data-ttu-id="b8e3d-150">Une fois le **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE**, le contenu de pièce jointe n’est pas dans le message.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="b8e3d-151">Au lieu de cela, la propriété **PR_ATTACH_LONG_FILENAME** contient une URL absolue pour le contenu de pièce jointe, qui est stocké en ligne.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b8e3d-152">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b8e3d-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8e3d-153">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b8e3d-153">Protocol specifications</span></span>

<span data-ttu-id="b8e3d-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8e3d-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8e3d-155">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8e3d-156">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b8e3d-156">Header files</span></span>

<span data-ttu-id="b8e3d-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8e3d-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8e3d-158">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8e3d-159">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b8e3d-159">Mapitags.h</span></span>
  
> <span data-ttu-id="b8e3d-160">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b8e3d-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8e3d-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8e3d-161">See also</span></span>



[<span data-ttu-id="b8e3d-162">Propriété canonique PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="b8e3d-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="b8e3d-163">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b8e3d-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8e3d-164">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b8e3d-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8e3d-165">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b8e3d-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8e3d-166">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b8e3d-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

