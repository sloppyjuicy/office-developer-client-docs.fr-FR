---
title: TNEF-Tagged texte du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419918"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="bb92e-103">TNEF-Tagged texte du message</span><span class="sxs-lookup"><span data-stu-id="bb92e-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="bb92e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb92e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb92e-105">Le texte du message marqué est utilisé par le TNEF pour résoudre les positions des pièces jointes dans le message parent.</span><span class="sxs-lookup"><span data-stu-id="bb92e-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="bb92e-106">Pour ce faire, ajoutez un titulaire de position dans le texte du message à la position de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="bb92e-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="bb92e-107">Ce support d’endroit, ou balise de pièce jointe, décrit la pièce jointe de telle sorte que le TNEF sache comment résoudre la pièce jointe et sa position.</span><span class="sxs-lookup"><span data-stu-id="bb92e-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="bb92e-108">Les balises sont formatées comme suit :</span><span class="sxs-lookup"><span data-stu-id="bb92e-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="bb92e-109">**\< Le \> titre de l’objet** et **\< le nom de \>** fichier sont des variables contenant des valeurs qui sont tirées de la pièce jointe elle-même.</span><span class="sxs-lookup"><span data-stu-id="bb92e-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="bb92e-110">Dans les cas où ces valeurs ne sont pas disponibles, le titre est par défaut TNEF en fonction du type de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="bb92e-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="bb92e-111">La variable **\< KeyNum \>** contient la représentation textuelle de la clé de pièce jointe affectée à la pièce jointe par le TNEF.</span><span class="sxs-lookup"><span data-stu-id="bb92e-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="bb92e-112">La valeur de base de la clé est transmise à [l’appel OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="bb92e-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="bb92e-113">La valeur de base ne doit pas être zéro et ne doit pas être identique pour chaque appel à **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="bb92e-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="bb92e-114">Il suffit d’utiliser des nombres pseudo-aléatoires en fonction de l’heure système à partir du générateur de nombres aléatoires que votre bibliothèque d’utilisation fournit, à condition que vous garantissez qu’ils ne sont jamais nuls.</span><span class="sxs-lookup"><span data-stu-id="bb92e-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="bb92e-115">La variable **\< Nom \>** de transport contient le nom du flux transmis à l’appel [OpenTnefStreamEx](opentnefstreamex.md) ou la valeur de la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb92e-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bb92e-116">La **PR_ATTACH_TRANSPORT_NAME** de transport et la variable **\< de \>** nom de transport dans une balise de texte de message n’ont rien à voir avec le nom du fournisseur de transport que vous implémentez.</span><span class="sxs-lookup"><span data-stu-id="bb92e-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="bb92e-117">Ces éléments représentent le nom d’une pièce jointe pour le fournisseur de transport et le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bb92e-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="bb92e-118">Le texte du message est balisé lorsqu’un fournisseur de transport demande un texte de message balisé en appelant la méthode [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="bb92e-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="bb92e-119">Lors de la lecture à partir du flux de texte balisé, TNEF remplace le caractère unique qui se trouvait dans le texte du message à l’index fourni dans la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) par la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="bb92e-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="bb92e-120">Lors de l’écriture dans le flux de texte balisé, le TNEF recherche les balises dans les données entrantes, recherche la pièce jointe associée et remplace la balise par un espace unique.</span><span class="sxs-lookup"><span data-stu-id="bb92e-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="bb92e-121">Notez qu’à l’aide de texte de message balisé, un fournisseur de transport peut conserver le positionnement des pièces jointes indépendamment de la plupart des modifications apportées au texte du message par les systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bb92e-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

