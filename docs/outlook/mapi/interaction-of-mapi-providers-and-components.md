---
title: Interaction des composants et des fournisseurs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592625"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="0aaba-103">Interaction des composants et des fournisseurs MAPI</span><span class="sxs-lookup"><span data-stu-id="0aaba-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="0aaba-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aaba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aaba-105">Fournisseurs de services MAPI de n’importe quel type doivent respecter certaines règles pour travailler avec d’autres composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="0aaba-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="0aaba-106">Chaque fournisseur de services doit :</span><span class="sxs-lookup"><span data-stu-id="0aaba-106">Each service provider must:</span></span>
  
- <span data-ttu-id="0aaba-107">Utiliser les objets de fournisseur et de connexion appropriés pour l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="0aaba-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="0aaba-108">Renvoie un tableau de répartition des points d’entrée fournisseur au système de messagerie lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="0aaba-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="0aaba-109">Enregistrer une ligne de tableau état MAPI pour chaque ressource détenu par le fournisseur et appelez la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) à des moments appropriés.</span><span class="sxs-lookup"><span data-stu-id="0aaba-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="0aaba-110">Utilisez la méthode [IMAPISupport::NewUID](imapisupport-newuid.md) pour obtenir les identificateurs uniques (UID) valides.</span><span class="sxs-lookup"><span data-stu-id="0aaba-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="0aaba-111">Prend en charge les interfaces MAPI courantes sur les objets qu’elle retourne.</span><span class="sxs-lookup"><span data-stu-id="0aaba-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="0aaba-112">Utilisez les fonctions d’allocation de mémoire MAPI d’allocation de mémoire renvoyé vers les applications clientes et libérer de la mémoire allouée par d’autres parties du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="0aaba-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="0aaba-113">Mettre à jour une section de profil, si nécessaire, pour stocker les informations d’identification pour le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0aaba-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="0aaba-114">Utilisez la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour inscrire les fonctions de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="0aaba-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="0aaba-115">Inclure les fichiers d’en-tête appropriés (y compris les mapispi.h) qui définissent les constantes communes, des structures, des interfaces et valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="0aaba-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="0aaba-116">Respecter les conventions de format d’adresse pour les types d’adresse.</span><span class="sxs-lookup"><span data-stu-id="0aaba-116">Follow address format conventions for common address types.</span></span>
    

