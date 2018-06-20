---
title: Développement d’un fournisseur de carnet d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783154"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="7e569-103">Développement d’un fournisseur de carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="7e569-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="7e569-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e569-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e569-105">Un fournisseur de carnet d’adresses fournit des informations de destinataires pour les applications clientes, à la banque de messages et fournisseurs, de transport et MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e569-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="7e569-106">Informations sur le destinataires sont organisées hiérarchiquement en compartiments de stockage appelés conteneurs.</span><span class="sxs-lookup"><span data-stu-id="7e569-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="7e569-107">Chaque carnet d’adresses dans le profil contribue à un ou plus niveau supérieur, ou parent, conteneurs MAPI carnet d’adresses, un affichage intégré d’informations sur le destinataires à partir de toutes les adresses du livre fournisseurs dans une session.</span><span class="sxs-lookup"><span data-stu-id="7e569-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="7e569-108">Il est par le biais du carnet d’adresses MAPI que les clients et autres fournisseurs de services accéder aux données d’un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7e569-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="7e569-109">MAPI génère le carnet d’adresses intégré par :</span><span class="sxs-lookup"><span data-stu-id="7e569-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="7e569-110">Récupérer les conteneurs de niveau supérieur à partir de chaque fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7e569-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="7e569-111">Extraction de table de hiérarchie de chaque conteneur.</span><span class="sxs-lookup"><span data-stu-id="7e569-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="7e569-112">Copie de chaque table de hiérarchie dans une table de hiérarchie intégré.</span><span class="sxs-lookup"><span data-stu-id="7e569-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="7e569-113">Il est la table de hiérarchie intégré qui est exposée au client.</span><span class="sxs-lookup"><span data-stu-id="7e569-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="7e569-114">MAPI impose certains éléments requis sur les auteurs de fournisseur adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="7e569-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="7e569-115">La gamme de fonctionnalités possibles que vous pouvez implémenter un enregistreur de carnet d’adresse est variés et flexibles.</span><span class="sxs-lookup"><span data-stu-id="7e569-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="7e569-116">Par exemple, votre fournisseur peut être limité à fournir une vue en lecture seule d’un type particulier d’informations sur le destinataires ou implémenter un ensemble complet de fonctionnalités, permettant ainsi peut-être des clients ou fournisseurs de faire des ajouts ou modifications aux données destinataires et d’imposer les critères de recherche pour définir des vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7e569-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="7e569-117">Les données de votre fournisseur peuvent résider localement dans un fichier de base de données ou sur un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="7e569-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="7e569-118">Certains fournisseurs de carnet d’adresses sont conçus pour fonctionner avec un système de messagerie particulier, fortement couplé à un fournisseur de transport, tandis que d’autres personnes peuvent fonctionner avec tout système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7e569-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="7e569-119">MAPI définit un type particulier de fournisseur de carnet d’adresses appelée un carnet d’adresses personnel ou le carnet d’adresses personnel, qui implémente un seul conteneur modifiable et peut contenir des informations sur les destinataires copiées à partir d’autres conteneurs, ainsi que les informations créées directement.</span><span class="sxs-lookup"><span data-stu-id="7e569-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="7e569-120">Bien que n’importe quel fournisseur de carnet d’adresses peut mettre en œuvre un carnet d’adresses personnel et plusieurs carnets d’adresses personnels peuvent être ajoutés à un profil, un seul de ces fournisseurs peut être désigné pour fonctionner en tant que le carnet d’adresses personnel pendant toute une session.</span><span class="sxs-lookup"><span data-stu-id="7e569-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

