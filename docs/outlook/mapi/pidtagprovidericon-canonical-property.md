---
title: Propriété canonique PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286459"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="3af21-103">Propriété canonique PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="3af21-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="3af21-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3af21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3af21-105">Contient une chaîne Unicode qui spécifie une icône personnalisée ou des icônes à afficher pour un fournisseur MAPI dans la barre d'état Microsoft Office Outlook dans les États en ligne et hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3af21-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3af21-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3af21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3af21-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="3af21-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="3af21-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3af21-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3af21-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="3af21-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="3af21-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3af21-110">Data type:</span></span>  <br/> |<span data-ttu-id="3af21-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3af21-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3af21-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3af21-112">Area:</span></span>  <br/> |<span data-ttu-id="3af21-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="3af21-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3af21-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3af21-114">Remarks</span></span>

<span data-ttu-id="3af21-115">Ces propriétés spécifient le fichier de ressources qui contient une icône personnalisée qui représente un fournisseur MAPI dans un État en ligne et, éventuellement, une autre icône personnalisée dans l'état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3af21-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="3af21-116">Outlook demande toujours ces propriétés dans la représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="3af21-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="3af21-117">Par exemple, la valeur de la propriété suivante demande à Outlook de charger l'ID d'icône 1001 à partir du module mymod32. dll et d'utiliser cette `mymod32.dll,#1001`icône pour l'État en ligne:.</span><span class="sxs-lookup"><span data-stu-id="3af21-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="3af21-118">Étant donné qu'il n'existe pas d'icône spécifique au fournisseur pour l'état hors connexion, dans ce cas, l'icône Outlook hors connexion standard est utilisée dans la barre d'État.</span><span class="sxs-lookup"><span data-stu-id="3af21-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="3af21-119">La valeur de la propriété suivante indique à Outlook de charger l'ID d'icône 1001 à partir du module mymod32. dll et d'utiliser cette icône pour l'État en ligne et de charger également l'ID d'icône 1002 à partir de ce `mymod32.dll,#1001,#1002`même module pour être utilisé pour l'état hors connexion:.</span><span class="sxs-lookup"><span data-stu-id="3af21-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="3af21-120">Aucune icône Outlook n'est utilisée dans la barre d'État.</span><span class="sxs-lookup"><span data-stu-id="3af21-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="3af21-121">Par défaut, si aucune icône personnalisée n'est spécifiée, le fournisseur est représenté par les icônes Outlook par défaut pour l'État en ligne et l'état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3af21-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="3af21-122">Le fournisseur peut éventuellement spécifier un nom complet à afficher en regard de l'icône dans la barre d'État.</span><span class="sxs-lookup"><span data-stu-id="3af21-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="3af21-123">Pour plus d'informations, voir **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3af21-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3af21-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="3af21-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3af21-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="3af21-125">Header files</span></span>

<span data-ttu-id="3af21-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3af21-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3af21-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3af21-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="3af21-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3af21-128">Mapitags.h</span></span>
  
> <span data-ttu-id="3af21-129">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="3af21-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3af21-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3af21-130">See also</span></span>



[<span data-ttu-id="3af21-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3af21-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3af21-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3af21-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3af21-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3af21-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3af21-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3af21-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

