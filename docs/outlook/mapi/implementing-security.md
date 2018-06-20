---
title: Implémentation de la sécurité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f09d96fd8b35df6cafa81b3830642cf6d67806e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784199"
---
# <a name="implementing-security"></a><span data-ttu-id="4a1b5-103">Implémentation de la sécurité</span><span class="sxs-lookup"><span data-stu-id="4a1b5-103">Implementing Security</span></span>

  
  
<span data-ttu-id="4a1b5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a1b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a1b5-105">Si le système de messagerie a besoin, le fournisseur de transport est responsable de la mise en œuvre d’un niveau de sécurité pour l’accès au système de messagerie approprié.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="4a1b5-106">Chaque message entrant ou sortant envoyé via un fournisseur de transport par le spouleur MAPI est géré dans le contexte d’une session d’ouverture de session du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="4a1b5-107">Le fournisseur de transport peut afficher une boîte de dialogue d’ouverture de session à l’utilisateur qui vous invite à fournir les informations d’identification d’un utilisateur avant d’établir une connexion de ce type.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="4a1b5-108">Sinon, le fournisseur de transport peut stocker les informations d’identification entrées précédemment dans la plage de la propriété sécurisée dans une section de profil et les utiliser pour l’accès sans demander de confirmation.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="4a1b5-109">Lorsque vous implémentez la sécurité de votre fournisseur de transport, considérez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="4a1b5-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="4a1b5-110">Avec plusieurs fournisseurs de service installé, il peut y avoir une multitude de noms et mots de passe associés à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="4a1b5-111">MAPI permet à plusieurs sessions avec plusieurs identités.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="4a1b5-112">Les fournisseurs sont invités à prendre en charge plusieurs sessions mais ne sont pas nécessaires à le faire.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="4a1b5-113">Chaque session avec un fournisseur de transport est associée à MAPI une section discrète dans le profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="4a1b5-114">Le fournisseur de transport peut utiliser la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour accéder à cette section, qui peut être utilisée pour stocker les informations relatives liés cette session, y compris les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="4a1b5-115">Avec plusieurs fournisseurs de transport installé, il n’est pas nécessairement vrai que l’utilisateur n’a qu’une adresse de messagerie unique.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="4a1b5-116">Un utilisateur peut avoir une adresse de messagerie distinct pour chaque fournisseur de transport installés ou permettre avoir une adresse différente pour chaque session sur un seul fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="4a1b5-117">Pour plus d’informations sur le stockage des informations d’identification dans les sections de profil, voir [Services de messagerie et les profils](message-services-and-profiles.md) et [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4a1b5-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

