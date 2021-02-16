---
title: Définition de l’ordre de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433597"
---
# <a name="setting-transport-order"></a><span data-ttu-id="1ad33-103">Définition de l’ordre de transport</span><span class="sxs-lookup"><span data-stu-id="1ad33-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="1ad33-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ad33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ad33-105">Lepooler MAPI attribue la responsabilité des messages sortants en fonction des types d’adresses et des identificateurs que les fournisseurs de transport déclarent qu’ils peuvent gérer.</span><span class="sxs-lookup"><span data-stu-id="1ad33-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="1ad33-106">Les fournisseurs de transport publient une liste de types d’adresses et d’identificateurs pris en charge , stockés dans des structures **MAPIUID,** lorsque MAPI appelle leur méthode [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) directement après l’ouverture de la demande.</span><span class="sxs-lookup"><span data-stu-id="1ad33-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="1ad33-107">Le type d’adresse d’un destinataire est stocké dans **sa PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1ad33-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="1ad33-108">L’inscription à un type d’adresse indique à MAPI que le fournisseur de transport peut remettre aux destinataires avec leur propriété **PR_ADDRTYPE** définie sur le type d’adresse enregistré.</span><span class="sxs-lookup"><span data-stu-id="1ad33-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="1ad33-109">De même, l’inscription à **un MAPIUID** indique que le fournisseur de transport peut remettre à des destinataires représentés par des identificateurs d’entrée avec le **MAPIUID enregistré.**</span><span class="sxs-lookup"><span data-stu-id="1ad33-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="1ad33-110">La plupart des fournisseurs de transport s’inscrivent pour un ou plusieurs types d’adresses ; quelques inscrits **par MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="1ad33-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="1ad33-111">Les fournisseurs de transport étroitement associés à un fournisseur de carnet d’adresses et qui comprennent son format d’identificateur d’entrée peuvent s’inscrire pour gérer les messages par **MAPIUID,** améliorant ainsi les performances.</span><span class="sxs-lookup"><span data-stu-id="1ad33-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="1ad33-112">Ces fournisseurs de transport étroitement couplés peuvent extraire l’adresse e-mail du destinataire et d’autres informations nécessaires de l’identificateur d’entrée sans avoir à l’ouvrir avec un appel **IMAPISupport::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="1ad33-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="1ad33-113">MAPI conserve une commande pour les fournisseurs de transport, utilisée lorsque plusieurs fournisseurs de transport se sont inscrits pour le même type d’adresse ou **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="1ad33-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="1ad33-114">Vous pouvez remplacer cet ordre en appelant [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) et en passant une liste triée des **MAPIUID** de tous les fournisseurs de transport actifs pointés par le paramètre  _lpUIDList_ :</span><span class="sxs-lookup"><span data-stu-id="1ad33-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID** s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="1ad33-115">Pour récupérer une liste de tous les types d’adresses qui peuvent être gérés par l’un des fournisseurs de transport actifs, appelez [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1ad33-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="1ad33-116">**EnumAdrTypes renvoie** un tableau de chaînes qui décrit les types d’adresses pris en charge par les fournisseurs de transport qui sont actifs dans la session active.</span><span class="sxs-lookup"><span data-stu-id="1ad33-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

