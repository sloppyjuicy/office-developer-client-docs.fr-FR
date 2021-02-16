---
title: Développement de serveurs de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420765"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="8132c-103">Développement de serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="8132c-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="8132c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8132c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8132c-105">Cette section décrit le processus de création de fichiers exécutables et de configuration de formulaires de serveur de formulaires pour la création de formulaires MAPI personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8132c-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="8132c-106">Avant de lire cette section, vous devez vous familiariser avec les informations des formulaires [MAPI.](mapi-forms.md)</span><span class="sxs-lookup"><span data-stu-id="8132c-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="8132c-107">Le développement d’un serveur de formulaire comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8132c-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="8132c-108">Choix des informations contenues dans le formulaire et choix d’un ensemble de propriétés pour contenir ces informations.</span><span class="sxs-lookup"><span data-stu-id="8132c-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="8132c-109">Pour plus d’informations, [voir Choosing a Form’s Property Set](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="8132c-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="8132c-110">Conception d’une interface utilisateur avec laquelle les utilisateurs peuvent interagir avec les propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8132c-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="8132c-111">Choix d’une classe de message et génération d’un identificateur de classe unique (CLSID).</span><span class="sxs-lookup"><span data-stu-id="8132c-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="8132c-112">Pour une vue d’ensemble des classes de message, voir [CLASSES de message MAPI.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="8132c-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="8132c-113">Pour plus d’informations sur les classes de message et les formulaires, voir [Choosing a Message Class](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="8132c-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="8132c-114">Implémenter les interfaces de formulaire MAPI requises, ainsi que les interfaces facultatives dont votre serveur de formulaires spécifique a besoin.</span><span class="sxs-lookup"><span data-stu-id="8132c-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="8132c-115">Pour plus d’informations, voir [Écrire du code serveur de formulaires.](writing-form-server-code.md)</span><span class="sxs-lookup"><span data-stu-id="8132c-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="8132c-116">Écriture de code d’interface utilisateur pour gérer l’interaction de l’utilisateur avec l’objet formulaire et les propriétés qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="8132c-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="8132c-117">Création d’un fichier de configuration de formulaire pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8132c-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="8132c-118">Pour plus d’informations, [voir Format de fichier des fichiers de configuration de formulaire.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="8132c-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="8132c-119">Installation du formulaire sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8132c-119">Installing the form on users' computers.</span></span> <span data-ttu-id="8132c-120">Pour plus d’informations, [voir Installation d’un formulaire dans une bibliothèque.](installing-a-form-into-a-library.md)</span><span class="sxs-lookup"><span data-stu-id="8132c-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="8132c-121">Vous effectuerez probablement les étapes 1 à 5 simultanément au lieu de les effectuer dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="8132c-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="8132c-122">Le processus de développement d’un serveur de formulaires, comme de nombreux projets de programmation, n’est pas celui dans lequel il existe une séquence particulièrement bien définie.</span><span class="sxs-lookup"><span data-stu-id="8132c-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="8132c-123">Par exemple, la création d’un fichier de configuration de formulaire s’affiche comme l’avant-dernière étape ci-dessus, mais vous créerez probablement votre fichier de configuration de formulaire de manière incrémentielle et il deviendra plus complet à mesure que vous ajouterez des fonctionnalités à votre serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="8132c-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8132c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8132c-124">See also</span></span>



[<span data-ttu-id="8132c-125">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="8132c-125">MAPI Concepts</span></span>](mapi-concepts.md)

