---
title: Types d'adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298011"
---
# <a name="mapi-address-types"></a><span data-ttu-id="1eac0-103">Types d'adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="1eac0-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="1eac0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1eac0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1eac0-105">Chaque utilisateur de messagerie est associé à un type d'adresse, une chaîne de caractères décrivant le format de l'adresse de l'utilisateur qui est stockée dans la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1eac0-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="1eac0-106">Les types d'adresses correspondent aux formats d'adresse.</span><span class="sxs-lookup"><span data-stu-id="1eac0-106">Address types map to address formats.</span></span> <span data-ttu-id="1eac0-107">En regardant le type d'adresse d'un destinataire, les applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="1eac0-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="1eac0-108">Par exemple, le `SMTP` type d'adresse spécifie l'adresse Internet standard:</span><span class="sxs-lookup"><span data-stu-id="1eac0-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="1eac0-109">Et le `EX` type d'adresse spécifie une adresse de serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="1eac0-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="1eac0-110">Toutes les entrées de carnet d'adresses doivent avoir un type d'adresse valide.</span><span class="sxs-lookup"><span data-stu-id="1eac0-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="1eac0-111">Les clients exigent que leurs utilisateurs spécifient un type d'adresse lors de la création d'un type de destinataire personnalisé non pris en charge par le fournisseur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="1eac0-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="1eac0-112">Pour les entrées qu'ils prennent en charge, les fournisseurs de carnet d'adresses doivent fournir des types d'adresses valides.</span><span class="sxs-lookup"><span data-stu-id="1eac0-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="1eac0-113">MAPI définit un seul type d'adresse: MAPIPDL, qui correspond à la liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="1eac0-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="1eac0-114">Pour obtenir la liste des types d'adresses pris en charge par tous les fournisseurs de transport dans la session, les applications clientes appellent la méthode **IMAPISession:: EnumAdrTypes** .</span><span class="sxs-lookup"><span data-stu-id="1eac0-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="1eac0-115">Pour plus d'informations, voir [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1eac0-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

