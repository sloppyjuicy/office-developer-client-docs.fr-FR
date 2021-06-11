---
title: Propriété canonique PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360738"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="456f9-103">Propriété canonique PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="456f9-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="456f9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="456f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="456f9-105">Contient le nom, le type de données et d’autres informations sur un champ défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="456f9-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="456f9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="456f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="456f9-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="456f9-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="456f9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="456f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="456f9-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="456f9-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="456f9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="456f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="456f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="456f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="456f9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="456f9-112">Area:</span></span>  <br/> |<span data-ttu-id="456f9-113">Dossier MAPI</span><span class="sxs-lookup"><span data-stu-id="456f9-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="456f9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="456f9-114">Remarks</span></span>

<span data-ttu-id="456f9-115">Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant.</span><span class="sxs-lookup"><span data-stu-id="456f9-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="456f9-116">La **propriété PidLidPropertyDefinitionStream** contient un flux binaire appelé [PropertyDefinition](propertydefinition-stream-structure.md), qui contient les définitions de champ.</span><span class="sxs-lookup"><span data-stu-id="456f9-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="456f9-117">Pour plus d’informations sur les structures de flux pour les définitions de champ, voir [Stream Structures](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="456f9-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="456f9-118">Pour chaque dossier, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans ce dossier dans la propriété **PidTagUserFields** d’un message associé de la classe de message IPC.MS. REN. USERFIELDS : chaque dossier supposé ne contenir qu’un seul message de cette classe dans la table des matières associée.</span><span class="sxs-lookup"><span data-stu-id="456f9-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="456f9-119">L’ensemble des champs définis par l’utilisateur dans un dossier peut ne pas nécessairement correspondre aux ensembles de champs définis par l’utilisateur dans chacun de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="456f9-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="456f9-120">L’ensemble des champs définis par l’utilisateur dans un dossier est affiché à différents endroits dans l’interface utilisateur Outlook, tels que le s’il s’agit du s’il s’agit du dossier.</span><span class="sxs-lookup"><span data-stu-id="456f9-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="456f9-121">La propriété **PidTagUserFields du** message contient un flux binaire, **FolderUserFields**, qui contient les définitions de champ de dossier.</span><span class="sxs-lookup"><span data-stu-id="456f9-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="456f9-122">Pour plus d’informations sur les structures de flux pour les définitions de champ de dossier, voir [Structures](folder-fields-stream-structures.md) de flux de champs de dossier et exemple de flux [FolderUserFields.](folderuserfields-stream-sample.md)</span><span class="sxs-lookup"><span data-stu-id="456f9-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="456f9-123">Titre de section</span><span class="sxs-lookup"><span data-stu-id="456f9-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="456f9-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="456f9-124">Protocol specifications</span></span>

<span data-ttu-id="456f9-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="456f9-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="456f9-126">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="456f9-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="456f9-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="456f9-127">Header files</span></span>

<span data-ttu-id="456f9-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="456f9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="456f9-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="456f9-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="456f9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="456f9-130">See also</span></span>



[<span data-ttu-id="456f9-131">Outlook Éléments et champs</span><span class="sxs-lookup"><span data-stu-id="456f9-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="456f9-132">Ajouter une définition pour un nouveau champ User-Defined de recherche</span><span class="sxs-lookup"><span data-stu-id="456f9-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="456f9-133">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="456f9-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="456f9-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="456f9-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="456f9-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="456f9-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="456f9-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="456f9-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="456f9-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="456f9-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

