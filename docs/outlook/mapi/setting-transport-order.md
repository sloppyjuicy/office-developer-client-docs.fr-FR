---
title: Ordre de Transport de paramètre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787141"
---
# <a name="setting-transport-order"></a><span data-ttu-id="0479b-103">Ordre de Transport de paramètre</span><span class="sxs-lookup"><span data-stu-id="0479b-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="0479b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0479b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0479b-105">Le spouleur MAPI attribue la responsabilité pour les messages sortants en fonction des types d’adresses et identificateurs de fournisseurs de transport déclarer qu’ils peuvent gérer.</span><span class="sxs-lookup"><span data-stu-id="0479b-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="0479b-106">Fournisseurs de transport publient une liste des types d’adresse pris en charge et les identificateurs, stockées dans des structures **MAPIUID** — lorsque MAPI appelle leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , directement après l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="0479b-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="0479b-107">Type d’adresse d’un destinataire est stocké dans sa propriété **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0479b-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0479b-108">Inscription pour un type d’adresse indique à MAPI que le fournisseur de transport peut remettre aux destinataires dont la propriété **TYPEADR_PR** définie sur le type d’adresse enregistrée.</span><span class="sxs-lookup"><span data-stu-id="0479b-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="0479b-109">De même, l’enregistrement pour un **MAPIUID** indique que le fournisseur de transport peut remettre à des destinataires qui sont représentées par les identificateurs d’entrée avec la inscrits **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="0479b-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="0479b-110">La plupart des fournisseurs de transport s’inscrire pour un ou plusieurs types d’adresses ; peu inscrire par **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="0479b-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="0479b-111">Fournisseurs de transport qui sont étroitement liés à un fournisseur de carnet d’adresses et de comprennent son format d’identificateur d’entrée peuvent s’inscrire pour gérer les messages par **MAPIUID**, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="0479b-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="0479b-112">Ces fournisseurs de transport étroitement couplés extraire adresse de messagerie du destinataire et d’autres informations nécessaires à partir de l’identificateur d’entrée sans avoir à ouvrir avec un appel **IMAPISupport::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="0479b-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="0479b-113">MAPI gère une commande pour les fournisseurs de transport, utilisée lorsque plusieurs fournisseurs de transport ont enregistré pour le même type d’adresse ou **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="0479b-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="0479b-114">Vous pouvez remplacer cet ordre en appelant [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) et en transmettant une liste triée des s **MAPIUID**de tous les fournisseurs de transport actif vers laquelle pointe le paramètre _lpUIDList_ . :</span><span class="sxs-lookup"><span data-stu-id="0479b-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="0479b-115">Pour récupérer une liste de tous les types d’adresses qui peuvent être gérés par un des fournisseurs de transport actif, appelez [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="0479b-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="0479b-116">**EnumAdrTypes** renvoie un tableau de chaînes qui décrit les types d’adresse pris en charge par les fournisseurs de transport qui sont actifs dans la session active.</span><span class="sxs-lookup"><span data-stu-id="0479b-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

