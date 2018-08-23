---
title: Bibliothèques de formulaires personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 546b45deaa856bbfa002797e491d9b47be0dd34a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581586"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="2b1a9-103">Bibliothèques de formulaires personnels</span><span class="sxs-lookup"><span data-stu-id="2b1a9-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="2b1a9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b1a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b1a9-105">Comme son nom l’indique, les bibliothèques de formulaires personnels contiennent des formulaires d’intérêt pour un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="2b1a9-106">Bibliothèque des formulaires personnels d’un utilisateur est la bibliothèque de formulaires associée à la banque de messages par défaut identifiée dans le profil de l’utilisateur ; chaque profil installé sur une station de travail peut utiliser un magasin distinct par défaut et par conséquent, une bibliothèque de formulaires personnels distincts.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="2b1a9-107">Une bibliothèque de formulaires personnels peut contenir les copies des formulaires qui figurent également dans les autres bibliothèques de formulaires en plus des autres formes.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="2b1a9-108">Une bibliothèque de formulaires personnels est implémentée dans le tableau contenu associé du dossier racine de la banque de messages par défaut d’un utilisateur — si qui réside sur un serveur ou localement sur le poste de travail est non significatifs.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="2b1a9-109">Si la banque de messages par défaut de l’utilisateur est stockée sur le poste de travail, bibliothèques de formulaires personnels offrent des performances améliorées en permettant aux applications d’accéder aux formulaires local au lieu de via le réseau.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="2b1a9-110">Il est également formulaires disponible pour les utilisateurs qui travaillent en mode hors connexion, qui peuvent se produire lorsque les utilisateurs souhaitent prendre leurs formulaires avec eux sur des ordinateurs portables et sont sans accès à un réseau.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="2b1a9-111">Les propriétés et l’implémentation sous-jacente des entrées de la bibliothèque des formulaires personnels incluent une propriété de « ID conteneur » qui identifie le conteneur principal qui l’entrée locale doit être synchronisée avec.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="2b1a9-112">Cela peut être l’identificateur d’un dossier arbitraire qui contienne les formulaires.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="2b1a9-113">Cette option est utile si vous utilisez un gestionnaire de formulaire personnalisé qui prend en charge un type de bibliothèque de formulaires de l’organisation ; le Gestionnaire de formulaire se chargera de synchroniser les formulaires stockés dans la bibliothèque de formulaires personnels et la bibliothèque de formulaires de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="2b1a9-114">Cela probablement se produit lorsque le Gestionnaire de formulaire a été chargé, mais il peut se produire théoriquement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b1a9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b1a9-115">See also</span></span>



[<span data-ttu-id="2b1a9-116">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="2b1a9-116">MAPI Forms</span></span>](mapi-forms.md)

