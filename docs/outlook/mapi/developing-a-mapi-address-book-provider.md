---
title: Développement d’un fournisseur de carnet d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409369"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="b0859-103">Développement d’un fournisseur de carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="b0859-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="b0859-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0859-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0859-105">Un fournisseur de carnet d’adresses fournit des informations sur les destinataires aux applications clientes, aux fournisseurs de magasins de messages et de transport, et à MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0859-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="b0859-106">Les informations sur les destinataires sont organisées hiérarchiquement en compartiments de stockage appelés conteneurs.</span><span class="sxs-lookup"><span data-stu-id="b0859-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="b0859-107">Chaque carnet d’adresses du profil contribue à un ou plusieurs conteneurs de niveau supérieur, ou parent, au carnet d’adresses MAPI, une vue intégrée des informations sur les destinataires de tous les fournisseurs de carnets d’adresses dans une session.</span><span class="sxs-lookup"><span data-stu-id="b0859-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="b0859-108">C’est par le biais du carnet d’adresses MAPI que les clients et autres fournisseurs de services ont accès aux données d’un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b0859-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="b0859-109">MAPI crée le carnet d’adresses intégré en :</span><span class="sxs-lookup"><span data-stu-id="b0859-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="b0859-110">Récupération des conteneurs de niveau supérieur de chaque fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b0859-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="b0859-111">Récupération de la table de hiérarchie de chaque conteneur.</span><span class="sxs-lookup"><span data-stu-id="b0859-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="b0859-112">Copie de chaque table de hiérarchie dans une table de hiérarchie intégrée.</span><span class="sxs-lookup"><span data-stu-id="b0859-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="b0859-113">Il s’agit de la table de hiérarchie intégrée qui est exposée au client.</span><span class="sxs-lookup"><span data-stu-id="b0859-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="b0859-114">MAPI impose peu d’exigences aux rédacteurs de fournisseurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b0859-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="b0859-115">La gamme de fonctionnalités possibles que vous pouvez implémenter en tant que rédacteur de carnet d’adresses est variée et flexible.</span><span class="sxs-lookup"><span data-stu-id="b0859-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="b0859-116">Par exemple, votre fournisseur peut être limité à fournir une vue en lecture seule d’un type particulier d’informations sur les destinataires ou implémenter un ensemble complet de fonctionnalités, ce qui peut permettre aux clients ou fournisseurs d’apporter des ajouts ou des modifications aux données des destinataires et d’imposer des critères de recherche pour définir des affichages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b0859-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="b0859-117">Les données de votre fournisseur peuvent résider localement dans un fichier ou une base de données ou sur un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="b0859-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="b0859-118">Certains fournisseurs de carnets d’adresses sont destinés à fonctionner avec un système de messagerie particulier, étroitement associé à un fournisseur de transport, tandis que d’autres peuvent fonctionner avec n’importe quel système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b0859-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="b0859-119">MAPI définit un type spécial de fournisseur de carnet d’adresses appelé carnet d’adresses personnel( PAB), qui implémente un conteneur modifiable unique et peut contenir des informations sur les destinataires copiées à partir d’autres conteneurs, ainsi que des informations créées directement.</span><span class="sxs-lookup"><span data-stu-id="b0859-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="b0859-120">Bien que n’importe quel fournisseur de carnet d’adresses puisse implémenter un carnet d’adresses en mode page et que plusieurs carnets d’adresses en mode sans fil peuvent être ajoutés à un profil, un seul de ces fournisseurs peut être désigné pour fonctionner en tant que carnet d’adresses en mode sans fil au cours d’une session.</span><span class="sxs-lookup"><span data-stu-id="b0859-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

