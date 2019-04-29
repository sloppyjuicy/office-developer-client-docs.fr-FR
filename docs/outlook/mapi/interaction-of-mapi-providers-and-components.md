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
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434661"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="53854-103">Interaction des composants et des fournisseurs MAPI</span><span class="sxs-lookup"><span data-stu-id="53854-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="53854-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53854-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53854-105">Les fournisseurs de services MAPI de tout type doivent respecter certaines recommandations pour fonctionner avec d'autres composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="53854-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="53854-106">Chaque fournisseur de services doit:</span><span class="sxs-lookup"><span data-stu-id="53854-106">Each service provider must:</span></span>
  
- <span data-ttu-id="53854-107">Utilisez le fournisseur et les objets d'ouverture de session appropriés pour l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="53854-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="53854-108">Renvoyer une table de répartition des points d'entrée de fournisseur vers le système de messagerie lors de l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="53854-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="53854-109">Enregistrez une ligne de table d'État MAPI pour chaque ressource appartenant au fournisseur et appelez la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) à des moments appropriés.</span><span class="sxs-lookup"><span data-stu-id="53854-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="53854-110">Utilisez la méthode [IMAPISupport:: NewUID](imapisupport-newuid.md) pour obtenir des identificateurs uniques valides (UID).</span><span class="sxs-lookup"><span data-stu-id="53854-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="53854-111">Prendre en charge les interfaces MAPI communes sur les objets qu'elle renvoie.</span><span class="sxs-lookup"><span data-stu-id="53854-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="53854-112">Utilisez les fonctions d'allocation de mémoire MAPI pour allouer de la mémoire renvoyée aux applications clientes et libérer la mémoire allouée par les autres composants du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="53854-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="53854-113">Gérer une section de profil, si nécessaire, pour stocker les informations d'identification dans le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="53854-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="53854-114">Utilisez la méthode [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour enregistrer les fonctions de prétraitement des messages.</span><span class="sxs-lookup"><span data-stu-id="53854-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="53854-115">Incluez les fichiers d'en-tête corrects (y compris mapispi. h) qui définissent les constantes, les structures, les interfaces et les valeurs de retour communes.</span><span class="sxs-lookup"><span data-stu-id="53854-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="53854-116">Respectez les conventions de format d'adresse pour les types d'adresse courants.</span><span class="sxs-lookup"><span data-stu-id="53854-116">Follow address format conventions for common address types.</span></span>
    

