---
title: Implémentation de la sécurité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310058"
---
# <a name="implementing-security"></a><span data-ttu-id="ec61a-103">Implémentation de la sécurité</span><span class="sxs-lookup"><span data-stu-id="ec61a-103">Implementing Security</span></span>

  
  
<span data-ttu-id="ec61a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec61a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec61a-105">Si le système de messagerie l'exige, le fournisseur de transport est responsable de l'implémentation d'un niveau de sécurité approprié pour l'accès au système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ec61a-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="ec61a-106">Chaque message entrant ou sortant envoyé par le biais d'un fournisseur de transport par le spouleur MAPI est géré dans le contexte d'une session de connexion du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ec61a-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="ec61a-107">Le fournisseur de transport peut afficher une boîte de dialogue de connexion à l'utilisateur qui demande les informations d'identification d'un utilisateur avant d'établir une telle connexion.</span><span class="sxs-lookup"><span data-stu-id="ec61a-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="ec61a-108">En guise d'alternative, le fournisseur de transport peut stocker les informations d'identification précédemment saisies de l'utilisateur dans la plage de propriétés sécurisée au sein d'une section de profil et les utiliser pour l'accès sans invite.</span><span class="sxs-lookup"><span data-stu-id="ec61a-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="ec61a-109">Lors de l'implémentation de la sécurité de votre fournisseur de transport, prenez en compte les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="ec61a-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="ec61a-110">Avec plusieurs fournisseurs de services installés, il peut y avoir une multitude de noms et de mots de passe associés à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec61a-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="ec61a-111">MAPI autorise plusieurs sessions avec plusieurs identités.</span><span class="sxs-lookup"><span data-stu-id="ec61a-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="ec61a-112">Les fournisseurs sont encouragés à prendre en charge plusieurs sessions, mais ne sont pas tenus de le faire.</span><span class="sxs-lookup"><span data-stu-id="ec61a-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="ec61a-113">Chaque session avec un fournisseur de transport est associée à MAPI avec une section discrète dans le profil de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec61a-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="ec61a-114">Le fournisseur de transport peut utiliser la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) pour accéder à cette section, qui peut être utilisée pour stocker les informations associées à cette session, notamment les informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="ec61a-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="ec61a-115">Avec plusieurs fournisseurs de transport installés, il n'est pas nécessairement vrai que l'utilisateur ne possède qu'une seule adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ec61a-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="ec61a-116">Un utilisateur peut avoir une adresse de messagerie distincte pour chaque fournisseur de transport installé ou peut avoir une adresse différente pour chaque session sur un fournisseur unique.</span><span class="sxs-lookup"><span data-stu-id="ec61a-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="ec61a-117">Pour plus d'informations sur le stockage des informations d'identification dans les sections de profil, consultez la rubrique [messages services and](message-services-and-profiles.md) Profiles and [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="ec61a-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

