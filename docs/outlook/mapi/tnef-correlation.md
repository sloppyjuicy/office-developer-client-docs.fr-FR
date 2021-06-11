---
title: Corrélation TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410370"
---
# <a name="tnef-correlation"></a><span data-ttu-id="b24c1-103">Corrélation TNEF</span><span class="sxs-lookup"><span data-stu-id="b24c1-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="b24c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b24c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b24c1-105">Certains systèmes de messagerie effectuent une vérification de corrélation sur n’importe quel flux TNEF (Transport-Neutral Encapsulation Format) joint à un message entrant pour vérifier que le flux TNEF appartient bien à ce message.</span><span class="sxs-lookup"><span data-stu-id="b24c1-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="b24c1-106">Cela implique de faire correspondre la valeur d’un champ dans l’en-tête du message entrant avec une copie de cette valeur stockée dans une propriété dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="b24c1-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="b24c1-107">Les valeurs qui sont probablement uniques pour chaque message, telles que les numéros d’ID de message, sont généralement utilisées pour cela.</span><span class="sxs-lookup"><span data-stu-id="b24c1-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="b24c1-108">Le transport ou la passerelle qui a créé le flux TNEF est chargé de choisir une valeur appropriée dans l’en-tête du message et de placer une copie dans une propriété appropriée avant de coder les propriétés du message sortant dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="b24c1-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="b24c1-109">Les passerelles ou les transports qui reçoivent le message peuvent ensuite extraire cette propriété du flux TNEF et vérifier que sa valeur correspond à la valeur du champ d’en-tête correspondant sur le message entrant.</span><span class="sxs-lookup"><span data-stu-id="b24c1-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="b24c1-110">Si les valeurs ne correspondent pas, la passerelle ou le transport doit ignorer le flux TNEF et traiter uniquement l’enveloppe de message native.</span><span class="sxs-lookup"><span data-stu-id="b24c1-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="b24c1-111">Ces vérifications sont prudents, car les clients de messagerie non MAPI peuvent joindre un fichier qui contient un flux TNEF d’un ancien message à un envoi, voire à un message non lié ; Si elle n’est pas vérifiée, une telle erreur peut entraîner la perte de texte du message.</span><span class="sxs-lookup"><span data-stu-id="b24c1-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="b24c1-112">La valeur de champ d’en-tête choisie doit être propre au message.</span><span class="sxs-lookup"><span data-stu-id="b24c1-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="b24c1-113">Il n’existe pas de champ d’en-tête fixe pour tous les systèmes de messagerie, car différents systèmes de messagerie utilisent des champs d’en-tête différents, mais généralement le système de messagerie affecte un identificateur unique au message, ce qui convient à cet effet.</span><span class="sxs-lookup"><span data-stu-id="b24c1-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="b24c1-114">Par exemple, les systèmes SMTP utilisent généralement l’en-tête MessageID, tandis que les systèmes X.400 utilisent généralement l IM_THIS_IPM de message.</span><span class="sxs-lookup"><span data-stu-id="b24c1-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

