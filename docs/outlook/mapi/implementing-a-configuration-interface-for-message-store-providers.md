---
title: Implémentation d'une interface de configuration pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332976"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="77928-103">Implémentation d'une interface de configuration pour les fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="77928-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="77928-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77928-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77928-105">Les fournisseurs de banque de messages doivent implémenter une interface qui permet à l'utilisateur de configurer le fournisseur de banque de messages pour qu'il s'exécute sur l'ordinateur de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77928-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="77928-106">En règle générale, le fournisseur de banque de messages est configuré lorsque le fournisseur de banque de messages est ajouté au profil d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77928-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="77928-107">L'interface de configuration du fournisseur de banque de messages gère généralement des tâches telles que la définition des noms d'utilisateur et des mots de passe pour les banques de messages protégées, le choix des chemins d'accès aux fichiers nécessaires et la création du mécanisme de stockage sous-jacent qu'il utilisera, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="77928-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="77928-108">L'interface de configuration que vous implémentez est accessible par le biais de points d'entrée supplémentaires dans la DLL de votre fournisseur de services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="77928-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="77928-109">Pour plus d'informations, consultez [la rubrique Configuration d'un service de messagerie](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="77928-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="77928-110">L'interface de configuration du fournisseur de banque de messages est la seule interface utilisateur qu'un fournisseur de banque de messages doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="77928-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77928-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77928-111">See also</span></span>



[<span data-ttu-id="77928-112">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="77928-112">Message Store Features</span></span>](message-store-features.md)

