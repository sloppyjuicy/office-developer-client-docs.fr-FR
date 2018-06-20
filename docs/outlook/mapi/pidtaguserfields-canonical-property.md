---
title: Propriété canonique PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786899"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="af4e6-103">Propriété canonique PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="af4e6-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="af4e6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af4e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af4e6-105">Contient le nom du type de données et autres informations sur un champ défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="af4e6-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af4e6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="af4e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af4e6-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="af4e6-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="af4e6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="af4e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af4e6-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="af4e6-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="af4e6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="af4e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="af4e6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="af4e6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="af4e6-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="af4e6-112">Area:</span></span>  <br/> |<span data-ttu-id="af4e6-113">Dossier MAPI</span><span class="sxs-lookup"><span data-stu-id="af4e6-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af4e6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="af4e6-114">Remarks</span></span>

<span data-ttu-id="af4e6-115">Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant.</span><span class="sxs-lookup"><span data-stu-id="af4e6-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="af4e6-116">La propriété **PidLidPropertyDefinitionStream** contient un flux binaire appelé [la définition PropertyDefinition](propertydefinition-stream-structure.md), qui contient les définitions de champ.</span><span class="sxs-lookup"><span data-stu-id="af4e6-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="af4e6-117">Pour plus d’informations sur les structures de flux de données pour les définitions de champ, voir [Les Structures de flux de données](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="af4e6-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="af4e6-118">Pour chaque dossier, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans ce dossier dans la propriété **PidTagUserFields** d’un message de la classe de message Outlook.AGINGPROPERTIES associé. REN. CHAMPS - chaque dossier censé contenir pas plus d’un message de cette classe dans sa table des matières associée.</span><span class="sxs-lookup"><span data-stu-id="af4e6-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af4e6-119">L’ensemble des champs définis par l’utilisateur dans un dossier correspondent ne peut-être pas nécessairement les jeux de champs définis par l’utilisateur dans chacun de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="af4e6-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="af4e6-120">Le jeu de champs définis par l’utilisateur dans un dossier est affiché à divers emplacements dans l’interface utilisateur Outlook, telles que sélecteur de champs du dossier.</span><span class="sxs-lookup"><span data-stu-id="af4e6-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="af4e6-121">La propriété **PidTagUserFields** du message contient un flux binaire, **FolderUserFields**, qui contient les définitions de champ dossier.</span><span class="sxs-lookup"><span data-stu-id="af4e6-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="af4e6-122">Pour plus d’informations sur les structures de flux de données pour les définitions de champ dossier voir [Dossier champs Stream Structures](folder-fields-stream-structures.md) et l' [Exemple de flux de données FolderUserFields](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="af4e6-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="af4e6-123">Titre de section</span><span class="sxs-lookup"><span data-stu-id="af4e6-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af4e6-124">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="af4e6-124">Protocol specifications</span></span>

<span data-ttu-id="af4e6-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af4e6-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af4e6-126">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="af4e6-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af4e6-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="af4e6-127">Header files</span></span>

<span data-ttu-id="af4e6-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af4e6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="af4e6-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="af4e6-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af4e6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af4e6-130">See also</span></span>



[<span data-ttu-id="af4e6-131">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="af4e6-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="af4e6-132">Ajoutez une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="af4e6-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="af4e6-133">Exemple de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="af4e6-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="af4e6-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="af4e6-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af4e6-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="af4e6-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af4e6-136">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="af4e6-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af4e6-137">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="af4e6-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

