---
title: Propriété canonique PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396665"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="6786f-103">Propriété canonique PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="6786f-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="6786f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6786f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6786f-105">Contient une chaîne de texte qui identifie la classe de message défini par l’expéditeur, par exemple IPM. Note.</span><span class="sxs-lookup"><span data-stu-id="6786f-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6786f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6786f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6786f-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="6786f-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="6786f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6786f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6786f-109">0x001A du jeu</span><span class="sxs-lookup"><span data-stu-id="6786f-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="6786f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6786f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6786f-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6786f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6786f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6786f-112">Area:</span></span>  <br/> |<span data-ttu-id="6786f-113">Common</span><span class="sxs-lookup"><span data-stu-id="6786f-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6786f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6786f-114">Remarks</span></span>

<span data-ttu-id="6786f-115">La classe de message indique le type du message.</span><span class="sxs-lookup"><span data-stu-id="6786f-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="6786f-116">Il détermine l’ensemble des propriétés définies pour le message, le type d’informations le message dans le cas contraire et comment gérer le message.</span><span class="sxs-lookup"><span data-stu-id="6786f-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="6786f-117">Ces propriétés contiennent des chaînes concaténées avec des périodes.</span><span class="sxs-lookup"><span data-stu-id="6786f-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="6786f-118">Chaque chaîne représente un niveau de sous-classer.</span><span class="sxs-lookup"><span data-stu-id="6786f-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="6786f-119">Par exemple, IPM. Remarque est une sous-classe de IPM et une superclasse de IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="6786f-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="6786f-120">Ces propriétés doivent contenir des caractères ASCII 32 à 127 et ne doivent pas se terminer par un point (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="6786f-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="6786f-121">Opérations de tri et de comparer doivent traiter comme une chaîne respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="6786f-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="6786f-122">La longueur maximale possible est de 255 caractères, mais afin de permettre à ajouter qualificateurs MAPI, il est recommandé que la longueur d’origine doivent être conservées sous 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="6786f-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="6786f-123">Chaque message est nécessaire pour fournir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6786f-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="6786f-124">En règle générale, l’application cliente création d’un nouveau message lui dès que [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6786f-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="6786f-125">Mais si la propriété n’a pas été définie lorsque le client appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md), la banque de messages définissez-le IPM.</span><span class="sxs-lookup"><span data-stu-id="6786f-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="6786f-126">Les valeurs définies par MAPI sont :</span><span class="sxs-lookup"><span data-stu-id="6786f-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="6786f-127">IPM et IPC sont destinés à être surclasse uniquement, et un message doit avoir au moins un qualificateur sous-classe ajouté avant d’être stockée ou envoyé.</span><span class="sxs-lookup"><span data-stu-id="6786f-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="6786f-128">Pour plus d’informations sur l’utilisation des classes de message, consultez [Classes de Message](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="6786f-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="6786f-129">Pour les listes de propriétés obligatoires et facultatifs pour les classes de message, consultez les sujets secondaires à propos des [Propriétés](message-properties-overview.md)de Message.</span><span class="sxs-lookup"><span data-stu-id="6786f-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="6786f-130">Une classe de message personnalisée peut définir des propriétés dans une plage réservée pour une utilisation avec cette classe de message uniquement.</span><span class="sxs-lookup"><span data-stu-id="6786f-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="6786f-131">Pour plus d’informations, consultez la rubrique [Sur les identificateurs de propriété](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6786f-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="6786f-132">Contrôle de classes de message qui reçoivent un message entrant de dossier est stocké dans.</span><span class="sxs-lookup"><span data-stu-id="6786f-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="6786f-133">Pour plus d’informations, voir la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="6786f-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="6786f-134">Pour plus d’informations sur l’utilisation des classes de messages avec des formulaires et des serveurs de formulaire, voir [choix d’une classe de Message](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="6786f-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6786f-135">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6786f-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6786f-136">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6786f-136">Protocol specifications</span></span>

<span data-ttu-id="6786f-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6786f-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6786f-138">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6786f-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6786f-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6786f-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6786f-140">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6786f-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6786f-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6786f-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6786f-142">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="6786f-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6786f-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6786f-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6786f-144">Spécifie les propriétés et les opérations qui sont autorisées pour la représentation des messages de messagerie et de télécopie de voix.</span><span class="sxs-lookup"><span data-stu-id="6786f-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6786f-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6786f-145">Header files</span></span>

<span data-ttu-id="6786f-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6786f-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="6786f-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6786f-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="6786f-148">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6786f-148">Mapitags.h</span></span>
  
> <span data-ttu-id="6786f-149">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6786f-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6786f-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6786f-150">See also</span></span>



[<span data-ttu-id="6786f-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6786f-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6786f-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6786f-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6786f-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6786f-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6786f-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6786f-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

