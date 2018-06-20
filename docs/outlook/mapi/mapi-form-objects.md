---
title: Objets de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784619"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="6ad93-103">Objets de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="6ad93-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="6ad93-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ad93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ad93-105">Objets de formulaire sont créés dynamiquement par les serveurs de formulaire afin d’afficher des messages spécifiques et permettre aux utilisateurs d’interagir avec eux.</span><span class="sxs-lookup"><span data-stu-id="6ad93-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="6ad93-106">Un objet form est, par conséquent, une instanciation de la classe dérivée [IMAPIForm](imapiformiunknown.md) qui est implémentée par le serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="6ad93-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="6ad93-107">Lorsqu’une application cliente ouvre un message, le serveur de formulaire pour cette classe de message crée un objet de formulaire pour gérer le message.</span><span class="sxs-lookup"><span data-stu-id="6ad93-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="6ad93-108">L’objet form crée son interface et affiche les propriétés du message de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6ad93-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="6ad93-109">L’objet de formulaire et son interface persiste jusqu'à ce que l’utilisateur le ferme.</span><span class="sxs-lookup"><span data-stu-id="6ad93-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="6ad93-110">L’objet de formulaire gère toutes les modifications dans les valeurs des propriétés du message.</span><span class="sxs-lookup"><span data-stu-id="6ad93-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="6ad93-111">En outre, les interfaces de formulaire MAPI définissent un mécanisme par lequel un objet form charger et afficher une série de messages.</span><span class="sxs-lookup"><span data-stu-id="6ad93-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="6ad93-112">Il s’agit d’un mécanisme d’efficacité, car cela évite le destruction inutile et la création d’objets de message et leurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="6ad93-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="6ad93-113">Lorsque demandée par le client de messagerie pour charger un autre message, l’objet de formulaire doit enregistrer toutes les modifications aux propriétés du message en cours.</span><span class="sxs-lookup"><span data-stu-id="6ad93-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="6ad93-114">Pour plus d’informations sur le point de vue d’une application client des objets de formulaire, voir [MAPI aux objets formulaire personnalisé](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6ad93-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ad93-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad93-115">See also</span></span>



[<span data-ttu-id="6ad93-116">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="6ad93-116">MAPI Forms</span></span>](mapi-forms.md)

