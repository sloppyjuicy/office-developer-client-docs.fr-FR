---
title: Propriété canonique PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 649490f18bb1a14a7056b49fd846e893fba304bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575209"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="1174a-103">Propriété canonique PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="1174a-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="1174a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1174a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1174a-105">Contient un décalage, en caractères, à utiliser dans le rendu d’une pièce jointe dans le texte du message principal.</span><span class="sxs-lookup"><span data-stu-id="1174a-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1174a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1174a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1174a-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="1174a-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="1174a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1174a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1174a-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="1174a-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="1174a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1174a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1174a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1174a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1174a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1174a-112">Area:</span></span>  <br/> |<span data-ttu-id="1174a-113">Pièce jointe MAPI</span><span class="sxs-lookup"><span data-stu-id="1174a-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1174a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1174a-114">Remarks</span></span>

<span data-ttu-id="1174a-115">Lorsque le décalage fourni est -1 (0xFFFFFFFF), la pièce jointe n’est pas restituée à l’aide de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1174a-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="1174a-116">Toutes les valeurs autres que -1 indiquent la position dans la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) à laquelle la pièce jointe doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="1174a-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="1174a-117">**Remarque** Le caractère indiqué par cette propriété dans **PR_BODY** est remplacé par la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1174a-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="1174a-118">Ce caractère est généralement un espace, bien qu’un espace réservé spéciale caractère peut également être utilisé.</span><span class="sxs-lookup"><span data-stu-id="1174a-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="1174a-119">Cette propriété est exprimée en caractères.</span><span class="sxs-lookup"><span data-stu-id="1174a-119">This property is expressed in characters.</span></span> <span data-ttu-id="1174a-120">Dans certains jeux de caractères, ce n’est pas équivalent à octets.</span><span class="sxs-lookup"><span data-stu-id="1174a-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="1174a-121">Les applications Unicode peuvent calculer la position en fonction de caractères codés sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="1174a-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="1174a-122">Applications définir de caractères codés sur deux octets (DBCS) doivent analyser le texte jusqu'à la valeur de cette propriété, car la représentation sous forme de leur caractère varie entre 1 et 2 octets par caractère.</span><span class="sxs-lookup"><span data-stu-id="1174a-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="1174a-123">Cette propriété ne doit pas être utilisée avec le texte RTF (RICH Text Format).</span><span class="sxs-lookup"><span data-stu-id="1174a-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="1174a-124">La position de rendu est indiquée au format RTF par une séquence d’échappement appelée l’espace réservé d’objet pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1174a-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="1174a-125">Cette séquence se compose de la chaîne `\objattph` suivi d’un seul caractère, généralement un espace, qui sera remplacé par le rendu de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1174a-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1174a-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1174a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1174a-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1174a-127">Protocol specifications</span></span>

<span data-ttu-id="1174a-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1174a-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1174a-129">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="1174a-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1174a-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1174a-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1174a-131">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1174a-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1174a-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1174a-132">Header files</span></span>

<span data-ttu-id="1174a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1174a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="1174a-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1174a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="1174a-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1174a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="1174a-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1174a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1174a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1174a-137">See also</span></span>



[<span data-ttu-id="1174a-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1174a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1174a-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1174a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1174a-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1174a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1174a-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1174a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

