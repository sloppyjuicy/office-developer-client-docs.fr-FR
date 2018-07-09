---
title: Développez serveurs de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783166"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="121a0-103">Développez serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="121a0-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="121a0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="121a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="121a0-105">Cette section décrit le processus de création du fichier exécutable du serveur de formulaire et les fichiers de configuration de formulaire pour la création de formulaires MAPI personnalisés.</span><span class="sxs-lookup"><span data-stu-id="121a0-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="121a0-106">Avant de lire cette section, vous devez vous familiariser avec les informations contenues dans les [Formulaires MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="121a0-107">Développement d’un serveur de formulaire comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="121a0-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="121a0-108">Déterminer quelles informations contiendrait le formulaire et en sélectionnant un ensemble de propriétés pour stocker ces informations.</span><span class="sxs-lookup"><span data-stu-id="121a0-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="121a0-109">Pour plus d’informations, voir [choix de la valeur de propriété d’un formulaire](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="121a0-110">Conception d’une interface utilisateur avec lequel les utilisateurs peuvent interagir avec les propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="121a0-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="121a0-111">Choix d’une classe de message et la génération d’un identificateur unique de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="121a0-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="121a0-112">Pour une vue d’ensemble des classes de messages, consultez [Les Classes de Message MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="121a0-113">Pour plus d’informations sur les formulaires et les classes de messages, voir [choix d’une classe de Message](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="121a0-114">Implémenter les interfaces de formulaire MAPI requises, ainsi que toutes les interfaces facultatifs qui a besoin de votre serveur de formulaire particulier.</span><span class="sxs-lookup"><span data-stu-id="121a0-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="121a0-115">Pour plus d’informations, voir [L’écriture de Code de formulaire serveur](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="121a0-116">Écriture de code pour gérer l’interaction de l’utilisateur avec l’objet de formulaire et les propriétés de l’interface utilisateur par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="121a0-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="121a0-117">Création d’un fichier de configuration de formulaire pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="121a0-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="121a0-118">Pour plus d’informations, voir [Fichier fichiers au Format de formulaire Configuration](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="121a0-119">Installation du formulaire sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="121a0-119">Installing the form on users' computers.</span></span> <span data-ttu-id="121a0-120">Pour plus d’informations, consultez [installation d’un formulaire dans une bibliothèque](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="121a0-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="121a0-121">Vous serez probablement effectuer les étapes 1 à 5 simultanément au lieu de les effectuer dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="121a0-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="121a0-122">Le processus de développement d’un serveur de formulaire, comme de nombreux projets de programmation, n’est pas est une séquence particulièrement bien définie.</span><span class="sxs-lookup"><span data-stu-id="121a0-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="121a0-123">Par exemple, création d’un fichier de configuration de formulaire est affiché comme la seconde à la dernière étape ci-dessus, mais vous allez probablement créer votre fichier de configuration de formulaire incrémentielle, et devient plus complète lorsque vous ajoutez des fonctionnalités à votre serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="121a0-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="121a0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="121a0-124">See also</span></span>



[<span data-ttu-id="121a0-125">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="121a0-125">MAPI Concepts</span></span>](mapi-concepts.md)

