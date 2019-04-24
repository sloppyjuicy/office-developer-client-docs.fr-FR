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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359262"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="26131-103">Propriété canonique PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="26131-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="26131-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26131-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26131-105">Contient une chaîne de texte qui identifie la classe de message définie par l'expéditeur, telle que IPM. Note.</span><span class="sxs-lookup"><span data-stu-id="26131-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26131-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="26131-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26131-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="26131-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="26131-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="26131-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26131-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="26131-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="26131-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="26131-110">Data type:</span></span>  <br/> |<span data-ttu-id="26131-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="26131-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="26131-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="26131-112">Area:</span></span>  <br/> |<span data-ttu-id="26131-113">Courant</span><span class="sxs-lookup"><span data-stu-id="26131-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26131-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="26131-114">Remarks</span></span>

<span data-ttu-id="26131-115">La classe de message spécifie le type du message.</span><span class="sxs-lookup"><span data-stu-id="26131-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="26131-116">Il détermine le jeu de propriétés défini pour le message, le type d'informations que le message achemine et la façon de gérer le message.</span><span class="sxs-lookup"><span data-stu-id="26131-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="26131-117">Ces propriétés contiennent des chaînes concaténées avec des points.</span><span class="sxs-lookup"><span data-stu-id="26131-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="26131-118">Chaque chaîne représente un niveau de sous-Class.</span><span class="sxs-lookup"><span data-stu-id="26131-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="26131-119">Par exemple, IPM. Note est une sous-classe de IPM et une superclasse de IPM. Note. private.</span><span class="sxs-lookup"><span data-stu-id="26131-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="26131-120">Ces propriétés doivent être constituées des caractères ASCII 32 à 127 et ne doivent pas se terminer par un point (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="26131-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="26131-121">Les opérations de tri et de comparaison doivent les traiter comme une chaîne ne respectant pas la casse.</span><span class="sxs-lookup"><span data-stu-id="26131-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="26131-122">La longueur maximale possible est de 255 caractères, mais pour permettre à la salle MAPI d'ajouter des qualificateurs, il est recommandé de conserver la longueur d'origine sous 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="26131-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="26131-123">Chaque message est requis pour fournir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="26131-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="26131-124">Normalement, l'application cliente qui crée un nouveau message le définit dès que [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) renvoie avec succès.</span><span class="sxs-lookup"><span data-stu-id="26131-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="26131-125">Toutefois, si la propriété n'a pas été définie lorsque le client appelle [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), la Banque de messages doit la définir sur IPM.</span><span class="sxs-lookup"><span data-stu-id="26131-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="26131-126">Les valeurs définies par MAPI sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="26131-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="26131-127">IPM et IPC sont destinés à être des superclasses uniquement, et un message doit avoir au moins un qualificateur de sous-classe ajouté avant d'être stocké ou envoyé.</span><span class="sxs-lookup"><span data-stu-id="26131-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="26131-128">Pour plus d'informations sur l'utilisation de la classe de message, consultez la rubrique [classes de message](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="26131-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="26131-129">Pour obtenir la liste des propriétés requises et facultatives pour les classes de message, reportez-vous aux sous-rubriques de la rubrique [about message Properties](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26131-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="26131-130">Une classe de message personnalisée peut définir les propriétés d'une plage réservée à utiliser avec cette classe de message uniquement.</span><span class="sxs-lookup"><span data-stu-id="26131-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="26131-131">Pour plus d'informations, consultez la rubrique [à propos](mapi-property-identifier-overview.md)des identificateurs de propriétés.</span><span class="sxs-lookup"><span data-stu-id="26131-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="26131-132">Les classes de message contrôlent le dossier de réception dans lequel un message entrant est stocké.</span><span class="sxs-lookup"><span data-stu-id="26131-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="26131-133">Pour plus d'informations, reportez-vous à la méthode [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="26131-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="26131-134">Pour plus d'informations sur l'utilisation de classes de message avec des serveurs de formulaires et de formulaires, voir [Choosing a message Class](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="26131-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="26131-135">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="26131-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26131-136">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="26131-136">Protocol specifications</span></span>

<span data-ttu-id="26131-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26131-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26131-138">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="26131-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26131-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26131-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26131-140">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="26131-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="26131-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26131-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26131-142">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="26131-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="26131-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26131-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26131-144">Spécifie les propriétés et les opérations autorisées pour la représentation des messages vocaux et de télécopie.</span><span class="sxs-lookup"><span data-stu-id="26131-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26131-145">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="26131-145">Header files</span></span>

<span data-ttu-id="26131-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="26131-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="26131-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="26131-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="26131-148">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="26131-148">Mapitags.h</span></span>
  
> <span data-ttu-id="26131-149">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="26131-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26131-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26131-150">See also</span></span>



[<span data-ttu-id="26131-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="26131-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26131-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="26131-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26131-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="26131-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26131-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="26131-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

