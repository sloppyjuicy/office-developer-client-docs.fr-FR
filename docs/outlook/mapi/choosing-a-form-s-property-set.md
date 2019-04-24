---
title: Sélection d’un ensemble de propriétés pour un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332059"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="18054-103">Sélection d’un ensemble de propriétés pour un formulaire</span><span class="sxs-lookup"><span data-stu-id="18054-103">Choosing a form's property set</span></span>

<span data-ttu-id="18054-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18054-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18054-105">Lorsque vous implémentez votre serveur de formulaire, vous devez disposer d'une propriété pour chaque information dont votre classe de message a besoin.</span><span class="sxs-lookup"><span data-stu-id="18054-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="18054-106">Ces propriétés peuvent être des propriétés MAPI prédéfinies ou des propriétés personnalisées que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="18054-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="18054-107">Pour plus d'informations sur l'utilisation des propriétés, voir [MAPI Property Overview](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="18054-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="18054-108">Votre fichier de configuration de formulaire contiendra une liste de propriétés que votre serveur de formulaire expose pour les applications clientes à utiliser, mais cela ne doit pas nécessairement être la liste complète des propriétés utilisées par votre serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="18054-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="18054-109">Les applications clientes utilisent généralement les propriétés exposées pour permettre aux utilisateurs de trier les messages d'un dossier ou de personnaliser leurs interfaces d'une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="18054-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="18054-110">MAPI dispose d'un grand ensemble de propriétés prédéfinies qui suffisent à la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="18054-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="18054-111">Toutefois, il arrivera qu'une classe de message personnalisée ait besoin d'une propriété non définie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="18054-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="18054-112">Vous pouvez utiliser des propriétés personnalisées pour étendre l'ensemble prédéfini MAPI de propriétés pour les informations spéciales que votre serveur de formulaire doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="18054-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="18054-113">Vous pouvez utiliser l'une des méthodes suivantes pour définir des propriétés personnalisées:</span><span class="sxs-lookup"><span data-stu-id="18054-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="18054-114">Choisissez un nom pour la propriété et utilisez la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir une balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="18054-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="18054-115">L'interface [IMAPIProp](imapipropiunknown.md) par le biais de laquelle vous appelez cette méthode provient du pointeur [IMessage](imessageimapiprop.md) transmis au serveur de formulaire lors de la création du message.</span><span class="sxs-lookup"><span data-stu-id="18054-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="18054-116">Notez que le nom de la propriété doit être une chaîne à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="18054-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="18054-117">Définissez une balise de propriété personnalisée vous-même.</span><span class="sxs-lookup"><span data-stu-id="18054-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="18054-118">Les balises de propriété personnalisée doivent être comprises dans la plage 0x6800 à 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="18054-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="18054-119">Les propriétés de cette plage sont spécifiques à la classe de messages.</span><span class="sxs-lookup"><span data-stu-id="18054-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="18054-120">Pour plus d'informations sur la définition des propriétés personnalisées, consultez la rubrique [Defining New MAPI Properties](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="18054-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="18054-121">Les serveurs de formulaire qui ont un texte de message utilisent souvent la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) pour le stocker.</span><span class="sxs-lookup"><span data-stu-id="18054-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="18054-122">Si votre serveur de formulaire utilise **PR_RTF_COMPRESSED**, il doit également s'assurer que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contient une version de texte uniquement du texte du message, dans le cas où le message résultant est lu par un client qui ne prend pas en charge le texte enrichi. Texte du message au format (RTF).</span><span class="sxs-lookup"><span data-stu-id="18054-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="18054-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18054-123">See also</span></span>

- [<span data-ttu-id="18054-124">Développement de serveurs de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="18054-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

