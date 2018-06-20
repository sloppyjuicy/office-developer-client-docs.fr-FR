---
title: Propriété canonique PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785236"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="3d71d-103">Propriété canonique PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="3d71d-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="3d71d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d71d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d71d-105">Spécifie comment générer et recalculer la valeur de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) lorsque propriétés modifier le nom de contact.</span><span class="sxs-lookup"><span data-stu-id="3d71d-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d71d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3d71d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d71d-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="3d71d-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="3d71d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3d71d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3d71d-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3d71d-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3d71d-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="3d71d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3d71d-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="3d71d-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="3d71d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3d71d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3d71d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d71d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d71d-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="3d71d-114">Area:</span></span>  <br/> |<span data-ttu-id="3d71d-115">Contact</span><span class="sxs-lookup"><span data-stu-id="3d71d-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d71d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d71d-116">Remarks</span></span>

<span data-ttu-id="3d71d-117">Si cette propriété est manquant ou une valeur non détaillés dans le tableau ci-dessous ou dans [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), l’application peut choisir sa propre logique de recalculer la valeur de la **dispidFileUnder** d' autres propriétés comme nom du contact.</span><span class="sxs-lookup"><span data-stu-id="3d71d-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="3d71d-118">Dans le tableau suivant, la notation <PropertyName> est utilisé pour spécifier « la valeur de PropertyName ».</span><span class="sxs-lookup"><span data-stu-id="3d71d-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="3d71d-119">Par exemple, si la valeur de la propriété **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) est « Smith », et la valeur de la propriété **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) est « Ben », puis «<PidTagGivenName> <PidTagSurname>» spécifie la chaîne « Ben Smith ».</span><span class="sxs-lookup"><span data-stu-id="3d71d-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="3d71d-120">Dans le tableau, « \r » spécifie un caractère de retour chariot, « \n » spécifie un caractère de saut de ligne, et <space> représente un espace.</span><span class="sxs-lookup"><span data-stu-id="3d71d-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="3d71d-121">**Valeur de la propriété **dispidFileUnderId****</span><span class="sxs-lookup"><span data-stu-id="3d71d-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="3d71d-122">**Description de la propriété **dispidFileUnder****</span><span class="sxs-lookup"><span data-stu-id="3d71d-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d71d-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d71d-123">0x00000000</span></span>  <br/> |<span data-ttu-id="3d71d-124">PT_UNICODE vide.</span><span class="sxs-lookup"><span data-stu-id="3d71d-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="3d71d-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="3d71d-125">0x00003001</span></span>  <br/> |<span data-ttu-id="3d71d-126">«\<PidTagDisplayName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="3d71d-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="3d71d-128">«\<PidTagGivenName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="3d71d-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="3d71d-130">«\<PidTagSurname\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="3d71d-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="3d71d-132">«\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="3d71d-133">0x00008017</span></span>  <br/> |<span data-ttu-id="3d71d-134">«\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="3d71d-135">0x00008018</span></span>  <br/> |<span data-ttu-id="3d71d-136">«\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="3d71d-137">0x00008019</span></span>  <br/> |<span data-ttu-id="3d71d-138">«\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="3d71d-139">0x00008030</span></span>  <br/> |<span data-ttu-id="3d71d-140">«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="3d71d-141">0x00008031</span></span>  <br/> |<span data-ttu-id="3d71d-142">«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="3d71d-143">0x00008032</span></span>  <br/> |<span data-ttu-id="3d71d-144">«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="3d71d-145">0x00008033</span></span>  <br/> |<span data-ttu-id="3d71d-146">«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="3d71d-147">0x00008034</span></span>  <br/> |<span data-ttu-id="3d71d-148">«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="3d71d-149">0x00008035</span></span>  <br/> |<span data-ttu-id="3d71d-150">«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="3d71d-151">0x00008036</span></span>  <br/> |<span data-ttu-id="3d71d-152">«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagGeneration\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="3d71d-153">0x00008037</span></span>  <br/> |<span data-ttu-id="3d71d-154">«\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagSurname\>\<espace\>\<PidTagGeneration\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="3d71d-155">0x00008038</span></span>  <br/> |<span data-ttu-id="3d71d-156">«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagGeneration\>»</span><span class="sxs-lookup"><span data-stu-id="3d71d-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3d71d-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="3d71d-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="3d71d-158">Spécifie que, lorsque vous affichez le contact, l’application doit essayer d’utiliser la valeur actuelle de **dispidFileUnder** et d’autres propriétés de contact pour rechercher « au mieux » **dispidFileUnderId** à une des valeurs dans le tableau précédents.</span><span class="sxs-lookup"><span data-stu-id="3d71d-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="3d71d-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="3d71d-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="3d71d-160">Spécifie que, lorsque vous affichez le contact, l’application doit choisir les valeurs par défaut approprié (en fonction des paramètres régionaux de langue) pour **dispidFileUnderId** et **dispidFileUnder** pour faire correspondre le choix de mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="3d71d-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="3d71d-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="3d71d-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="3d71d-162">**dispidFileUnder** est une PT_UNICODE fourni par l’utilisateur et ne doit pas être modifiée lors de la modification d’une autre propriété nom du contact.</span><span class="sxs-lookup"><span data-stu-id="3d71d-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3d71d-163">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3d71d-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d71d-164">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3d71d-164">Protocol specifications</span></span>

<span data-ttu-id="3d71d-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d71d-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d71d-166">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="3d71d-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d71d-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d71d-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d71d-168">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="3d71d-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d71d-169">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3d71d-169">Header files</span></span>

<span data-ttu-id="3d71d-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d71d-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d71d-171">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3d71d-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d71d-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d71d-172">See also</span></span>



[<span data-ttu-id="3d71d-173">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3d71d-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d71d-174">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3d71d-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d71d-175">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3d71d-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d71d-176">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3d71d-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

