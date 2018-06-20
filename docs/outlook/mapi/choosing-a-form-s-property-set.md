---
title: Choix du jeu de propriétés d’un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 456ef036b26fd8b9840d33f0f699474c3a6ce127
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783042"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="67ea5-103">Choix du jeu de propriétés d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="67ea5-103">Choosing a form's property set</span></span>

<span data-ttu-id="67ea5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67ea5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67ea5-105">Lorsque vous implémentez votre serveur de formulaire, vous devez avoir une propriété pour chaque élément d’information qui a besoin de votre classe de message.</span><span class="sxs-lookup"><span data-stu-id="67ea5-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="67ea5-106">Ces propriétés peuvent être des propriétés MAPI prédéfinies, ou ils peuvent être des propriétés personnalisées que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="67ea5-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="67ea5-107">Pour plus d’informations sur l’utilisation des propriétés, voir [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="67ea5-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="67ea5-108">Votre fichier de configuration de formulaire contient une liste des propriétés qui expose de votre serveur de formulaire pour les applications clientes à utiliser, mais il ne doit pas être la liste complète des propriétés utilisées par le serveur de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="67ea5-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="67ea5-109">Applications clientes utilisent généralement les propriétés exposées pour permettre aux utilisateurs de classer les messages dans un dossier ou personnaliser leurs interfaces d’une manière.</span><span class="sxs-lookup"><span data-stu-id="67ea5-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="67ea5-110">MAPI a un grand ensemble de propriétés prédéfinies qui suffit pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="67ea5-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="67ea5-111">Toutefois, il peut arriver lorsqu’une classe de message personnalisée doit être une propriété qui ne définit pas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="67ea5-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="67ea5-112">Vous pouvez utiliser les propriétés personnalisées pour étendre l’ensemble MAPI prédéfinie des propriétés pour les informations spéciales que votre serveur de formulaire doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="67ea5-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="67ea5-113">Vous pouvez utiliser une des méthodes suivantes pour définir des propriétés personnalisées :</span><span class="sxs-lookup"><span data-stu-id="67ea5-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="67ea5-114">Choisissez un nom pour la propriété et la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) permet d’obtenir une balise de propriété pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="67ea5-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="67ea5-115">L’interface [IMAPIProp](imapipropiunknown.md) par le biais de laquelle vous appelez cette méthode provient le pointeur [IMessage](imessageimapiprop.md) qui est transmis au serveur de formulaire lorsque le message est créé.</span><span class="sxs-lookup"><span data-stu-id="67ea5-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="67ea5-116">Notez que le nom de la propriété doit être une chaîne de caractères étendus.</span><span class="sxs-lookup"><span data-stu-id="67ea5-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="67ea5-117">Définir une balise de propriété personnalisée vous-même.</span><span class="sxs-lookup"><span data-stu-id="67ea5-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="67ea5-118">Balises de propriété personnalisée doivent être dans la plage 0x6800 via 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="67ea5-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="67ea5-119">Les propriétés de cette plage sont classe de message spécifique.</span><span class="sxs-lookup"><span data-stu-id="67ea5-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="67ea5-120">Pour plus d’informations sur la définition des propriétés personnalisées, voir [Définition des nouvelles propriétés MAPI](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="67ea5-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="67ea5-121">Serveurs de formulaire qui ont un texte de message souvent permet de stocker la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="67ea5-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="67ea5-122">Si votre serveur formulaire utilise **PR_RTF_COMPRESSED**, il doit également vous assurer que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contient une version texte seul du texte du message, au cas où le message qui en résulte est lu par un client qui ne prend pas en charge le texte riche Texte du message au format RTF.</span><span class="sxs-lookup"><span data-stu-id="67ea5-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67ea5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67ea5-123">See also</span></span>

- [<span data-ttu-id="67ea5-124">Développez serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="67ea5-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

