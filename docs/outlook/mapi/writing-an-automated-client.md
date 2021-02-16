---
title: Écriture d’un client automatisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439764"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="c7a59-103">Écriture d’un client automatisé</span><span class="sxs-lookup"><span data-stu-id="c7a59-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="c7a59-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7a59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7a59-105">Une application cliente automatisée est une application qui s’exécute sans surveillance et n’affiche aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7a59-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="c7a59-106">Par défaut, de nombreuses méthodes d’interface MAPI montrent une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7a59-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="c7a59-107">Toutes ces méthodes ont des indicateurs qui permettent à un client d’autoriser ou de supprimer cet affichage.</span><span class="sxs-lookup"><span data-stu-id="c7a59-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="c7a59-108">Bien que MAPI s’attende à ce que les fournisseurs de services respectent ces indicateurs, certains fournisseurs ne répondent pas toujours à ces attentes.</span><span class="sxs-lookup"><span data-stu-id="c7a59-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="c7a59-109">Une raison légitime de ne pas respecter les indicateurs est la dépendance du fournisseur de services vis-à-vis d’un autre service qui n’autorise pas la suppression de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7a59-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="c7a59-110">Si vous développez un client automatisé, faites attention aux fournisseurs de services que vous utilisez et à leur configuration.</span><span class="sxs-lookup"><span data-stu-id="c7a59-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="c7a59-111">Ne supposez pas que tous vos appels pour supprimer une interface utilisateur seront réussis.</span><span class="sxs-lookup"><span data-stu-id="c7a59-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="c7a59-112">Les clients automatisés doivent avoir les informations nécessaires pour une configuration appropriée de chacun des services de message dans le profil.</span><span class="sxs-lookup"><span data-stu-id="c7a59-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="c7a59-113">Il existe deux façons de fournir des informations de configuration au moment de l’logo :</span><span class="sxs-lookup"><span data-stu-id="c7a59-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="c7a59-114">Le fournisseur de services peut récupérer des informations à partir du profil.</span><span class="sxs-lookup"><span data-stu-id="c7a59-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="c7a59-115">Le fournisseur de services peut fournir des informations à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7a59-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="c7a59-116">Étant donné que la deuxième option n’est pas disponible pour les clients automatisés, ces clients doivent utiliser la première option.</span><span class="sxs-lookup"><span data-stu-id="c7a59-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="c7a59-117">Les clients doivent configurer leurs profils avec soin pour s’assurer que cette option fonctionne toujours.</span><span class="sxs-lookup"><span data-stu-id="c7a59-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="c7a59-118">Les clients automatisés définissent toujours l MAPI_NO_MAIL dans l’appel de fonction [MAPILogonEx](mapilogonex.md) pour démarrer une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="c7a59-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

