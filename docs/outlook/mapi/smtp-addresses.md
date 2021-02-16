---
title: Adresses SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419624"
---
# <a name="smtp-addresses"></a><span data-ttu-id="13b14-103">Adresses SMTP</span><span class="sxs-lookup"><span data-stu-id="13b14-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="13b14-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b14-105">Le format des adresses de messagerie SMTP est défini dans la RFC 822.</span><span class="sxs-lookup"><span data-stu-id="13b14-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="13b14-106">Les composants MAPI doivent gérer n’importe quelle adresse conforme à cette norme.</span><span class="sxs-lookup"><span data-stu-id="13b14-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="13b14-107">Toutefois, il existe une forme particulière d’adresse RFC 822 qui code le mieux les adresses MAPI :</span><span class="sxs-lookup"><span data-stu-id="13b14-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="13b14-108">_display-name_ **\<** _email-address_**\>**</span><span class="sxs-lookup"><span data-stu-id="13b14-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="13b14-109">Les crochets sont inclus en tant que littéraux.</span><span class="sxs-lookup"><span data-stu-id="13b14-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="13b14-110">Les espaces vides sont courants dans les noms d’affichage ; Ils n’ont pas besoin d’être entre eux.</span><span class="sxs-lookup"><span data-stu-id="13b14-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="13b14-111">Une adresse type peut ressembler à celle-ci, qui appartient à l’un des co-auteurs de la RFC 1521 :</span><span class="sxs-lookup"><span data-stu-id="13b14-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="13b14-112">Nsb@bellcore.com \<\></span><span class="sxs-lookup"><span data-stu-id="13b14-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="13b14-113">Si le nom complet contient des caractères qui ont une signification spéciale dans les adresses SMTP, telles que @, le nom complet doit être entre \< guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="13b14-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="13b14-114">Sur le courrier sortant, si la longueur totale de l’adresse de messagerie et du nom complet dépasse 255 caractères, le nom complet doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="13b14-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="13b14-115">Les composants d’une adresse SMTP sont mappés dans les propriétés MAPI comme suit :</span><span class="sxs-lookup"><span data-stu-id="13b14-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="13b14-116">**Composant d’adresse SMTP**</span><span class="sxs-lookup"><span data-stu-id="13b14-116">**SMTP address component**</span></span>|<span data-ttu-id="13b14-117">**Propriété MAPI**</span><span class="sxs-lookup"><span data-stu-id="13b14-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="13b14-118">_nom complet de_ tous les destinataires</span><span class="sxs-lookup"><span data-stu-id="13b14-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="13b14-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13b14-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="13b14-120">_nom complet du_ champ De</span><span class="sxs-lookup"><span data-stu-id="13b14-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="13b14-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13b14-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="13b14-122">_nom complet du_ champ Expéditeur</span><span class="sxs-lookup"><span data-stu-id="13b14-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="13b14-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13b14-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="13b14-124">_email-address_</span><span class="sxs-lookup"><span data-stu-id="13b14-124">_email-address_</span></span> <br/> |<span data-ttu-id="13b14-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13b14-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="13b14-126">implicite, toujours « SMTP »</span><span class="sxs-lookup"><span data-stu-id="13b14-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="13b14-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13b14-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="13b14-128">S’il n’existe pas de nom complet pour une adresse sur le courrier entrant, l’adresse e-mail entière doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="13b14-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="13b14-129">Le type d’adresse est toujours SMTP.</span><span class="sxs-lookup"><span data-stu-id="13b14-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="13b14-130">Les propriétés du destinataire sont tirées de la table des destinataires du message MAPI . les propriétés de l’expéditeur sont tirées du message lui-même.</span><span class="sxs-lookup"><span data-stu-id="13b14-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

