---
title: Corrélation TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Dernière modification : 12 mars 2013'
ms.openlocfilehash: 5b5af5cee7c58eb300e4020c763431fd96bdd295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563760"
---
# <a name="tnef-correlation"></a><span data-ttu-id="c8090-103">Corrélation TNEF</span><span class="sxs-lookup"><span data-stu-id="c8090-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="c8090-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8090-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8090-105">Certains systèmes de messagerie effectuent une vérification de corrélation sur n’importe quel flux de Transport-Neutral Encapsulation Format (TNEF) joint à un message entrant pour vérifier que le flux TNEF appartient à ce message.</span><span class="sxs-lookup"><span data-stu-id="c8090-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="c8090-106">Cela implique correspondant à la valeur d’un champ dans l’en-tête du message entrant avec une copie de cette valeur stockée dans une propriété dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="c8090-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="c8090-107">Les valeurs qui sont probablement uniques pour chaque message, tels que les numéros d’identification de message, sont généralement utilisés pour ce.</span><span class="sxs-lookup"><span data-stu-id="c8090-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="c8090-108">Le transport ou la passerelle qui a créé le flux TNEF est chargé de choisir une valeur appropriée à partir de l’en-tête du message et placer une copie dans une propriété appropriée avant le codage des propriétés du message sortant dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="c8090-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="c8090-109">Passerelles ou des transports qui reçoivent le message peuvent ensuite extraire cette propriété à partir du flux TNEF et vérifiez que sa valeur correspond à la valeur du champ d’en-tête du message entrant correspondant.</span><span class="sxs-lookup"><span data-stu-id="c8090-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="c8090-110">Si les valeurs ne correspondent pas, la passerelle ou le transport doit ignorer le processus uniquement l’enveloppe du message native et les flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="c8090-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="c8090-111">Ces contrôles sont prudents, car les clients de messagerie non basé sur MAPI peuvent joindre un fichier qui contient un flux TNEF à partir d’un message ancien pour un transfert ou même un message indépendant ; s’il est ne pas activé, cette erreur risque d’entraîner la perte de texte du message.</span><span class="sxs-lookup"><span data-stu-id="c8090-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="c8090-112">La valeur du champ en-tête choisie doit être unique au message.</span><span class="sxs-lookup"><span data-stu-id="c8090-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="c8090-113">Il n’existe aucun champ d’en-tête fixe pour tous les systèmes de messagerie, car les différents systèmes de messagerie utilisent des champs d’en-tête différents, mais généralement le système de messagerie assigne un identificateur unique pour le message qui convient à cette fin.</span><span class="sxs-lookup"><span data-stu-id="c8090-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="c8090-114">Par exemple, systèmes SMTP utilisent généralement l’en-tête MessageID, tandis que les systèmes X.400 utilisent généralement l’attribut IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="c8090-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

