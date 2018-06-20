---
title: Types d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784558"
---
# <a name="mapi-address-types"></a><span data-ttu-id="84052-103">Types d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="84052-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="84052-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84052-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84052-105">Chaque utilisateur de messagerie est associé à un type d’adresse, une chaîne de caractères décrivant le format d’adresse de l’utilisateur qui est stocké dans la propriété **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84052-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="84052-106">Mappent les types d’adresses pour les formats d’adresse.</span><span class="sxs-lookup"><span data-stu-id="84052-106">Address types map to address formats.</span></span> <span data-ttu-id="84052-107">Autrement dit, en examinant le type d’adresse d’un destinataire, applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="84052-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="84052-108">Par exemple, le `SMTP` type d’adresse spécifie l’adresse Internet standard :</span><span class="sxs-lookup"><span data-stu-id="84052-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="84052-109">Et la `EX` type d’adresse spécifie une adresse de serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="84052-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="84052-110">Toutes les entrées de carnet d’adresses doivent avoir un type d’adresse valide.</span><span class="sxs-lookup"><span data-stu-id="84052-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="84052-111">Ils ont besoin de leurs utilisateurs spécifier un type d’adresse lors de la création d’un type de destinataire personnalisé non pris en charge par le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="84052-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="84052-112">Les entrées prises en charge, les fournisseurs de carnet d’adresses sont requis pour fournir des types d’adresses.</span><span class="sxs-lookup"><span data-stu-id="84052-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="84052-113">MAPI définit le type d’une seule adresse : MAPIPDL, ce qui signifie pour une liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="84052-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="84052-114">Pour obtenir une liste des types d’adresse pris en charge par tous les fournisseurs de transport dans la session, les applications clientes appellent la méthode **IMAPISession::EnumAdrTypes** .</span><span class="sxs-lookup"><span data-stu-id="84052-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="84052-115">Pour plus d’informations, voir [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="84052-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

