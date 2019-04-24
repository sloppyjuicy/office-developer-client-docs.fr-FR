---
title: Adresses SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344561"
---
# <a name="smtp-addresses"></a><span data-ttu-id="e155b-103">Adresses SMTP</span><span class="sxs-lookup"><span data-stu-id="e155b-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="e155b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e155b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e155b-105">Le format des adresses de messagerie SMTP est défini dans la norme RFC 822.</span><span class="sxs-lookup"><span data-stu-id="e155b-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="e155b-106">Les composants MAPI doivent gérer toute adresse conforme à cette norme.</span><span class="sxs-lookup"><span data-stu-id="e155b-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="e155b-107">Toutefois, il existe une forme particulière d'adresse RFC 822 qui code le mieux pour les adresses MAPI:</span><span class="sxs-lookup"><span data-stu-id="e155b-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="e155b-108">_nom d'affichage_ **\<** _adresse de messagerie_**\>**</span><span class="sxs-lookup"><span data-stu-id="e155b-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="e155b-109">Les chevrons sont inclus sous forme de littéraux.</span><span class="sxs-lookup"><span data-stu-id="e155b-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="e155b-110">Les espaces sont courants dans les noms d'affichage; ils n'ont pas besoin d'être cités.</span><span class="sxs-lookup"><span data-stu-id="e155b-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="e155b-111">Une adresse classique peut ressembler à celle-ci, qui appartient à l'un des coauteurs de la norme RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="e155b-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="e155b-112">Nathaniel Borenstein \<NSB@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="e155b-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="e155b-113">Si le nom d'affichage contient des caractères qui ont une signification particulière dans des adresses \< SMTP, par exemple, ou @, l'intégralité du nom complet doit être placée entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="e155b-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="e155b-114">Pour le courrier sortant, si la longueur totale de l'adresse de messagerie et du nom d'affichage dépasse 255 caractères, le nom d'affichage doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="e155b-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="e155b-115">Les parties d'une adresse SMTP sont mappées aux propriétés MAPI de la manière suivante:</span><span class="sxs-lookup"><span data-stu-id="e155b-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="e155b-116">**Composant d'adresse SMTP**</span><span class="sxs-lookup"><span data-stu-id="e155b-116">**SMTP address component**</span></span>|<span data-ttu-id="e155b-117">**Propriété MAPI**</span><span class="sxs-lookup"><span data-stu-id="e155b-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e155b-118">_nom d'affichage_ de tous les destinataires</span><span class="sxs-lookup"><span data-stu-id="e155b-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="e155b-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e155b-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="e155b-120">_nom d'affichage_ du champ de</span><span class="sxs-lookup"><span data-stu-id="e155b-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="e155b-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e155b-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="e155b-122">_nom d'affichage_ du champ sender</span><span class="sxs-lookup"><span data-stu-id="e155b-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="e155b-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e155b-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="e155b-124">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="e155b-124">_email-address_</span></span> <br/> |<span data-ttu-id="e155b-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e155b-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e155b-126">implicite, Always "SMTP"</span><span class="sxs-lookup"><span data-stu-id="e155b-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="e155b-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e155b-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="e155b-128">S'il n'existe pas de nom d'affichage pour une adresse sur le courrier entrant, l'adresse de messagerie complète doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="e155b-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="e155b-129">Le type d'adresse est toujours SMTP.</span><span class="sxs-lookup"><span data-stu-id="e155b-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="e155b-130">Les propriétés de destinataire sont extraites de la table de destinataires du message MAPI; les propriétés des expéditeurs sont extraites du message lui-même.</span><span class="sxs-lookup"><span data-stu-id="e155b-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

