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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0a4fdb94877fb9491005fc650c206ffefd3f8b94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578415"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="5e4ae-103">Propriété canonique PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="5e4ae-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="5e4ae-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e4ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e4ae-105">Spécifie comment générer et recalculer la valeur de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) lorsque propriétés modifier le nom de contact.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e4ae-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5e4ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e4ae-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="5e4ae-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="5e4ae-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5e4ae-108">Property set:</span></span>  <br/> |<span data-ttu-id="5e4ae-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5e4ae-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5e4ae-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="5e4ae-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5e4ae-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="5e4ae-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="5e4ae-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5e4ae-112">Data type:</span></span>  <br/> |<span data-ttu-id="5e4ae-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5e4ae-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5e4ae-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5e4ae-114">Area:</span></span>  <br/> |<span data-ttu-id="5e4ae-115">Contact</span><span class="sxs-lookup"><span data-stu-id="5e4ae-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e4ae-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e4ae-116">Remarks</span></span>

<span data-ttu-id="5e4ae-117">Si cette propriété est manquant ou une valeur non détaillés dans le tableau ci-dessous ou dans [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), l’application peut choisir sa propre logique de recalculer la valeur de la **dispidFileUnder** d' autres propriétés comme nom du contact.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="5e4ae-118">Dans le tableau suivant, la notation <PropertyName> est utilisé pour spécifier « la valeur de PropertyName ».</span><span class="sxs-lookup"><span data-stu-id="5e4ae-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="5e4ae-119">Par exemple, si la valeur de la propriété **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) est « Smith », et la valeur de la propriété **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) est « Ben », puis «<PidTagGivenName> <PidTagSurname>» spécifie la chaîne « Ben Smith ».</span><span class="sxs-lookup"><span data-stu-id="5e4ae-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="5e4ae-120">Dans le tableau, « \r » spécifie un caractère de retour chariot, « \n » spécifie un caractère de saut de ligne, et <space> représente un espace.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="5e4ae-121">**Valeur de la propriété **dispidFileUnderId****</span><span class="sxs-lookup"><span data-stu-id="5e4ae-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="5e4ae-122">**Description de la propriété **dispidFileUnder****</span><span class="sxs-lookup"><span data-stu-id="5e4ae-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e4ae-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e4ae-123">0x00000000</span></span>  <br/> |<span data-ttu-id="5e4ae-124">PT_UNICODE vide.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="5e4ae-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="5e4ae-125">0x00003001</span></span>  <br/> |<span data-ttu-id="5e4ae-126">«\<PidTagDisplayName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="5e4ae-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="5e4ae-128">«\<PidTagGivenName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="5e4ae-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="5e4ae-130">«\<PidTagSurname\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="5e4ae-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="5e4ae-132">«\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="5e4ae-133">0x00008017</span></span>  <br/> |<span data-ttu-id="5e4ae-134">«\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="5e4ae-135">0x00008018</span></span>  <br/> |<span data-ttu-id="5e4ae-136">«\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="5e4ae-137">0x00008019</span></span>  <br/> |<span data-ttu-id="5e4ae-138">«\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="5e4ae-139">0x00008030</span></span>  <br/> |<span data-ttu-id="5e4ae-140">«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="5e4ae-141">0x00008031</span></span>  <br/> |<span data-ttu-id="5e4ae-142">«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="5e4ae-143">0x00008032</span></span>  <br/> |<span data-ttu-id="5e4ae-144">«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="5e4ae-145">0x00008033</span></span>  <br/> |<span data-ttu-id="5e4ae-146">«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="5e4ae-147">0x00008034</span></span>  <br/> |<span data-ttu-id="5e4ae-148">«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="5e4ae-149">0x00008035</span></span>  <br/> |<span data-ttu-id="5e4ae-150">«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="5e4ae-151">0x00008036</span></span>  <br/> |<span data-ttu-id="5e4ae-152">«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagGeneration\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="5e4ae-153">0x00008037</span></span>  <br/> |<span data-ttu-id="5e4ae-154">«\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagSurname\>\<espace\>\<PidTagGeneration\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="5e4ae-155">0x00008038</span></span>  <br/> |<span data-ttu-id="5e4ae-156">«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagGeneration\>»</span><span class="sxs-lookup"><span data-stu-id="5e4ae-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="5e4ae-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="5e4ae-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="5e4ae-158">Spécifie que, lorsque vous affichez le contact, l’application doit essayer d’utiliser la valeur actuelle de **dispidFileUnder** et d’autres propriétés de contact pour rechercher « au mieux » **dispidFileUnderId** à une des valeurs dans le tableau précédents.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="5e4ae-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="5e4ae-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="5e4ae-160">Spécifie que, lorsque vous affichez le contact, l’application doit choisir les valeurs par défaut approprié (en fonction des paramètres régionaux de langue) pour **dispidFileUnderId** et **dispidFileUnder** pour faire correspondre le choix de mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="5e4ae-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5e4ae-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="5e4ae-162">**dispidFileUnder** est une PT_UNICODE fourni par l’utilisateur et ne doit pas être modifiée lors de la modification d’une autre propriété nom du contact.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5e4ae-163">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5e4ae-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e4ae-164">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5e4ae-164">Protocol specifications</span></span>

<span data-ttu-id="5e4ae-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e4ae-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e4ae-166">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e4ae-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e4ae-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e4ae-168">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e4ae-169">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5e4ae-169">Header files</span></span>

<span data-ttu-id="5e4ae-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e4ae-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e4ae-171">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5e4ae-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e4ae-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e4ae-172">See also</span></span>



[<span data-ttu-id="5e4ae-173">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5e4ae-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e4ae-174">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5e4ae-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e4ae-175">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5e4ae-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e4ae-176">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5e4ae-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

