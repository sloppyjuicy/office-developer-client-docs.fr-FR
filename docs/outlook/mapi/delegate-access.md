---
title: Acc�s d�l�gu�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427261"
---
# <a name="delegate-access"></a><span data-ttu-id="444a7-103">Accès délégué</span><span class="sxs-lookup"><span data-stu-id="444a7-103">Delegate Access</span></span>

  
  
<span data-ttu-id="444a7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="444a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="444a7-p101">Acc�s d�l�gu� fait r�f�rence � la capacit� de l'utilisateur pour envoyer un message sous la forme d'un autre utilisateur ou de recevoir un message pour un autre utilisateur. Acc�s d�l�gu� est une fonctionnalit� d'ind�pendant du fournisseur de service de MAPI prises en charge par les fournisseurs de transport s'ils le souhaitent. Toutefois, aucun fournisseur n'est requis pour effectuer cette op�ration. Acc�s d�l�gu� est utile lorsqu'il est n�cessaire pour un utilisateur d'envoyer des messages en tant qu'ou filtrer les messages entrants pour un autre utilisateur ou lorsqu'un utilisateur doit acc�der banque de messages d'un autre utilisateur. Avant d'autoriser un utilisateur d�l�gu� pour se connecter au magasin d'un autre utilisateur, le fournisseur de banque de messages doit v�rifier que l'utilisateur d�l�gu� dispose de l'autorit� appropri�e.</span><span class="sxs-lookup"><span data-stu-id="444a7-p101">Delegate access refers to the user's ability to send a message as another user or receive a message for another user. Delegate access is a service provider-independent feature of MAPI that transport providers can support if they choose. However, no provider is required to do so. Delegate access is valuable when it is necessary for a user to send messages as, or filter incoming messages for, another user or when a user must access another user's message store. Before allowing a delegate user to connect to another user's store, the message store provider must verify that the delegate user has the proper authority.</span></span> 
  
<span data-ttu-id="444a7-110">Il existe deux groupes de propri�t�s qui sont utilis�es pour prendre en charge l'acc�s d�l�gu� :</span><span class="sxs-lookup"><span data-stu-id="444a7-110">There are two groups of properties that are used to support delegate access:</span></span>
  
 <span data-ttu-id="444a7-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="444a7-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="444a7-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span></span> 
  
<span data-ttu-id="444a7-p102">Pour les messages sortants, les propri�t�s **PR_SENT_REPRESENTING** identifient l'utilisateur de messagerie qui doit agir en tant que l'exp�diteur. Les clients peuvent d�finir ces propri�t�s en tant qu'option. Si les propri�t�s **PR_SENT_REPRESENTING** ne sont pas d�finies au moment o� le message n'atteigne un fournisseur de transport qui prend en charge l'acc�s d�l�gu�, il incombe du fournisseur de les d�finir en m�me temps que les propri�t�s de **PR_SENDER**.</span><span class="sxs-lookup"><span data-stu-id="444a7-p102">On outgoing messages, the **PR_SENT_REPRESENTING** properties identify the messaging user that should act as the sender. Clients can set these properties as an option. If the **PR_SENT_REPRESENTING** properties are not set by the time the message reaches a transport provider that supports delegate access, it is the provider's responsibility to set them along with the **PR_SENDER** properties.</span></span> 
  
<span data-ttu-id="444a7-p103">Dans les messages entrants, les propri�t�s **PR_RCVD_REPRESENTING** identifient l'utilisateur qui doit agir en tant que le destinataire. Fournisseurs de transport responsable de la remise des messages de d�l�gu� doivent d�finir les propri�t�s de la **PR_RCVD_REPRESENTING** et **PR_RECEIVED_BY**. Clients re�oit un message de d�l�gu� doivent copier les valeurs des propri�t�s **PR_SENT_REPRESENTING** dans les propri�t�s correspondantes de **PR_RCVD_REPRESENTING**.</span><span class="sxs-lookup"><span data-stu-id="444a7-p103">On incoming messages, the **PR_RCVD_REPRESENTING** properties identify the user that should act as the recipient. Transport providers responsible for delivering delegate messages must set both the **PR_RCVD_REPRESENTING** and **PR_RECEIVED_BY** properties. Clients receiving a delegate message should copy the values of the **PR_SENT_REPRESENTING** properties to the corresponding **PR_RCVD_REPRESENTING** properties.</span></span> 
  
<span data-ttu-id="444a7-p104">Par exemple, supposons que John re�oit les messages de Sabine tandis que Sabine est en vacances. Les propri�t�s **PR_RCVD_REPRESENTING** identifient John en tant que le destinataire de d�l�gu�. Lorsque Jean envoie une r�ponse � un message � laquelle il a �t� de Sabine, les propri�t�s de message **PR_SENDER** identifient Jean comme l'exp�diteur du message. �tant donn� que John est repr�sentant Sabine, les propri�t�s **PR_SENT_REPRESENTING** identifient Sabine.</span><span class="sxs-lookup"><span data-stu-id="444a7-p104">For example, suppose John is receiving Sally's messages while Sally is on vacation. The **PR_RCVD_REPRESENTING** properties identify John as the delegate recipient. When John sends a reply to a message that he has received for Sally, the message's **PR_SENDER** properties identify John as the sender. Because John is representing Sally, the **PR_SENT_REPRESENTING** properties identify Sally.</span></span> 
  
<span data-ttu-id="444a7-p105">G�rer les messages entrants de d�l�gu� doivent remettre g�n�ralement ces messages en tant que l'utilisateur de messagerie identifi� par les propri�t�s **PR_SENT_REPRESENTING** et non en tant que l'utilisateur identifi� par les propri�t�s **PR_SENDER** des fournisseurs de transport. L'exception � cette r�gle est lorsqu'il est n�cessaire faire correspondre les types d'acc�s avec des privil�ges et de transport. Dans ce cas, un fournisseur de transport peut choisir une identit� d'envoi.</span><span class="sxs-lookup"><span data-stu-id="444a7-p105">Transport providers handling incoming delegate messages should usually deliver these messages as the messaging user identified by the **PR_SENT_REPRESENTING** properties rather than as the user identified by the **PR_SENDER** properties. The exception to this rule is when it is necessary to match access privilege and transport types. In this case, a transport provider can choose a sending identity.</span></span> 
  
<span data-ttu-id="444a7-p106">Si les propri�t�s **PR_SENT_REPRESENTING** ne sont pas disponibles pour un message entrant de d�l�gu�, le fournisseur de transport g�re la remise devez les d�finir, en utilisant les valeurs des propri�t�s **PR_SENDER** correspondante. Si les propri�t�s **PR_SENT_REPRESENTING** sont disponibles, mais le fournisseur de transport ne prend pas en charge l'acc�s d�l�gu�, il peut utiliser les propri�t�s de **PR_SENDER** pour la livraison.</span><span class="sxs-lookup"><span data-stu-id="444a7-p106">If the **PR_SENT_REPRESENTING** properties are unavailable for an incoming delegate message, the transport provider handling delivery must set them, using the values of the corresponding **PR_SENDER** properties. If the **PR_SENT_REPRESENTING** properties are available but the transport provider does not support delegate access, it can use the **PR_SENDER** properties for delivery.</span></span> 
  

