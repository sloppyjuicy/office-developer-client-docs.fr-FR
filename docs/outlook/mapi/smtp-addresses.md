---
title: Adresses SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 655d48d1ea937659f85e0ef7379425759ea7e256
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591358"
---
# <a name="smtp-addresses"></a><span data-ttu-id="352b8-103">Adresses SMTP</span><span class="sxs-lookup"><span data-stu-id="352b8-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="352b8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="352b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="352b8-105">Le format des adresses de messagerie SMTP est défini dans RFC 822.</span><span class="sxs-lookup"><span data-stu-id="352b8-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="352b8-106">Composants MAPI doivent gérer n’importe quelle adresse conforme à ce standard.</span><span class="sxs-lookup"><span data-stu-id="352b8-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="352b8-107">Toutefois, il existe un formulaire particulier d’adresse RFC 822 mieux encode adresses MAPI :</span><span class="sxs-lookup"><span data-stu-id="352b8-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="352b8-108">_nom d’affichage_ **\<** _- adresse de messagerie_**\>**</span><span class="sxs-lookup"><span data-stu-id="352b8-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="352b8-109">Les crochets sont inclus comme des caractères littéraux.</span><span class="sxs-lookup"><span data-stu-id="352b8-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="352b8-110">Les espaces sont courants dans les noms d’affichage ; ils ne doivent pas mis entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="352b8-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="352b8-111">Une adresse peut ressembler à celui-ci, qui appartient à un des co-auteurs de RFC 1521 :</span><span class="sxs-lookup"><span data-stu-id="352b8-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="352b8-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="352b8-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="352b8-113">Si le nom d’affichage contienne des caractères qui ont une signification spéciale dans les adresses SMTP, tel que \< ou @, le nom de la totalité de l’affichage doit être placée entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="352b8-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="352b8-114">Dans les messages sortants, si l’affichage de la longueur totale de l’adresse de messagerie plu nom dépasse 255 caractères, le nom complet doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="352b8-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="352b8-115">Les composants d’une adresse SMTP sont mappées à des propriétés MAPI, comme suit :</span><span class="sxs-lookup"><span data-stu-id="352b8-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="352b8-116">**Composant d’adresse SMTP**</span><span class="sxs-lookup"><span data-stu-id="352b8-116">**SMTP address component**</span></span>|<span data-ttu-id="352b8-117">**Propriété MAPI**</span><span class="sxs-lookup"><span data-stu-id="352b8-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="352b8-118">_nom d’affichage_ pour tous les destinataires</span><span class="sxs-lookup"><span data-stu-id="352b8-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="352b8-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="352b8-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="352b8-120">_nom d’affichage_ du champ</span><span class="sxs-lookup"><span data-stu-id="352b8-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="352b8-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="352b8-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="352b8-122">_nom d’affichage_ pour le champ de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="352b8-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="352b8-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="352b8-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="352b8-124">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="352b8-124">_email-address_</span></span> <br/> |<span data-ttu-id="352b8-125">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="352b8-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="352b8-126">implicites, toujours « SMTP »</span><span class="sxs-lookup"><span data-stu-id="352b8-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="352b8-127">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="352b8-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="352b8-128">S’il n’existe aucun nom d’affichage pour une adresse sur le courrier entrant, l’adresse de messagerie entière doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="352b8-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="352b8-129">Le type d’adresse est toujours SMTP.</span><span class="sxs-lookup"><span data-stu-id="352b8-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="352b8-130">Propriétés de destinataire proviennent de la table des destinataires du message MAPI ; propriétés de l’expéditeur sont prises dans le message lui-même.</span><span class="sxs-lookup"><span data-stu-id="352b8-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

