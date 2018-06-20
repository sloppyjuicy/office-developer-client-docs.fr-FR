---
title: Texte du Message TNEF balisés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787362"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="70e18-103">Texte du Message TNEF balisés</span><span class="sxs-lookup"><span data-stu-id="70e18-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="70e18-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70e18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70e18-105">Texte du message avec balise est utilisé par TNEF pour résoudre les positions des pièces jointes dans le message parent.</span><span class="sxs-lookup"><span data-stu-id="70e18-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="70e18-106">Cette opération est effectuée en ajoutant un espace réservé dans le texte du message à la position de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="70e18-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="70e18-107">Cet espace réservé ou balise de pièce jointe, décrit la pièce jointe de telle sorte que TNEF sait comment résoudre la pièce jointe et sa position.</span><span class="sxs-lookup"><span data-stu-id="70e18-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="70e18-108">Les balises sont mis en forme comme suit :</span><span class="sxs-lookup"><span data-stu-id="70e18-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="70e18-109">** \<Objet titre\> ** et ** \<nom de fichier\> ** sont des variables qui contiennent des valeurs qui proviennent de la pièce jointe elle-même.</span><span class="sxs-lookup"><span data-stu-id="70e18-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="70e18-110">Dans les cas où ces valeurs ne sont pas disponibles, le titre par défaut est celle par TNEF en fonction du type de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="70e18-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="70e18-111">Le ** \<KeyNum\> ** variable contient la représentation textuelle de la clé de pièce jointe associée à la pièce jointe par le format TNEF.</span><span class="sxs-lookup"><span data-stu-id="70e18-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="70e18-112">La valeur de la clé de base est transmise à l’appel de [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="70e18-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="70e18-113">La valeur de base ne doit pas être zéro et ne doit pas être la même pour chaque appel à **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="70e18-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="70e18-114">Elle devrait suffire pour utiliser des nombres aléatoires pseudo en fonction de l’heure système dans le Générateur de nombres aléatoires votre bibliothèque d’exécution fournit, dans la mesure où vous assurer qu’ils ne sont jamais zéro.</span><span class="sxs-lookup"><span data-stu-id="70e18-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="70e18-115">Le ** \<nom Transport\> ** variable contient le nom de flux de données passé dans l’appel [OpenTnefStreamEx](opentnefstreamex.md) ou la valeur de la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="70e18-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="70e18-116">La propriété **PR_ATTACH_TRANSPORT_NAME** et ** \<nom Transport\> ** variable dans une balise de texte de message n’a rien à voir avec le nom du fournisseur de transport que vous implémentez.</span><span class="sxs-lookup"><span data-stu-id="70e18-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="70e18-117">Ces éléments représentent le nom d’une pièce jointe pour le fournisseur de transport et le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="70e18-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="70e18-118">Le texte du message est marqué à la demande à un fournisseur de transport pour le texte du message avec balise en appelant la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="70e18-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="70e18-119">Lors de la lecture à partir du flux de texte référencé, TNEF remplace le caractère unique dans le texte du message à l’index fourni dans la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) avec la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="70e18-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="70e18-120">Lors de l’écriture dans le flux de texte référencé, TNEF vérifie les données entrantes pour les balises, trouve la pièce jointe associée et remplace la balise par un seul espace.</span><span class="sxs-lookup"><span data-stu-id="70e18-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="70e18-121">Notez que, en utilisant le texte du message avec balise, un fournisseur de transport permettre conserver le positionnement des pièces jointes quelle que soit la plupart des modifications apportées au texte du message par les systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="70e18-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

