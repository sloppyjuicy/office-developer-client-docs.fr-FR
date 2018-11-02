---
title: Implémentation d’une interface de configuration pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592926"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="04bd3-103">Implémentation d’une interface de configuration pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="04bd3-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="04bd3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04bd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04bd3-105">Fournisseurs de magasins de message sont requis pour implémenter une interface qui permet à l’utilisateur de configurer le fournisseur de banque de messages à exécuter sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04bd3-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="04bd3-106">En règle générale, le fournisseur de banque de messages est configuré lorsque le fournisseur de banque de message est ajouté à un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04bd3-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="04bd3-107">Interface de configuration du fournisseur de banque de messages gère généralement les tâches telles que la définition des noms d’utilisateur et mots de passe pour les magasins de message protégé, choix des chemins d’accès aux fichiers nécessaires, et création de mécanisme de stockage sous-jacent qu’il utilise, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="04bd3-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="04bd3-108">Vous implémentez l’interface de configuration est accessible via les points d’entrée supplémentaires dans une DLL de votre fournisseur de service de message.</span><span class="sxs-lookup"><span data-stu-id="04bd3-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="04bd3-109">Pour plus d’informations, voir [configuration d’un Service de Message](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="04bd3-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="04bd3-110">Interface de configuration du fournisseur de banque de messages est la seule interface utilisateur qu’un fournisseur de magasin de message doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="04bd3-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04bd3-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04bd3-111">See also</span></span>



[<span data-ttu-id="04bd3-112">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="04bd3-112">Message Store Features</span></span>](message-store-features.md)

