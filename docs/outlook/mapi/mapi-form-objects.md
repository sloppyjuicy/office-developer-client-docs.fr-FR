---
title: Objets de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351463"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="34463-103">Objets de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="34463-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="34463-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34463-105">Les objets de formulaire sont créés dynamiquement par les serveurs de formulaires afin d'afficher des messages spécifiques et d'autoriser les utilisateurs à interagir avec eux.</span><span class="sxs-lookup"><span data-stu-id="34463-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="34463-106">Un objet Form est, par conséquent, une instanciation de la classe dérivée de [IMAPIForm](imapiformiunknown.md) qui est implémentée par le serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="34463-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="34463-107">Lorsqu'une application cliente ouvre un message, le serveur de formulaire pour cette classe de message crée un objet Form pour gérer le message.</span><span class="sxs-lookup"><span data-stu-id="34463-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="34463-108">L'objet Form crée ensuite son interface et affiche les propriétés du message qu'elle contient.</span><span class="sxs-lookup"><span data-stu-id="34463-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="34463-109">L'objet Form et son interface persistent jusqu'à ce que l'utilisateur le ferme.</span><span class="sxs-lookup"><span data-stu-id="34463-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="34463-110">L'objet Form gère toutes les modifications apportées aux valeurs des propriétés du message.</span><span class="sxs-lookup"><span data-stu-id="34463-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="34463-111">En outre, les interfaces de formulaire MAPI définissent un mécanisme par lequel un objet Form peut charger et afficher une série de messages.</span><span class="sxs-lookup"><span data-stu-id="34463-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="34463-112">Il s'agit d'un mécanisme efficace, car il évite la destruction et la création d'objets message et de leurs interfaces inutiles.</span><span class="sxs-lookup"><span data-stu-id="34463-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="34463-113">Lorsque le client de messagerie le demande de charger un autre message, l'objet Form doit enregistrer les modifications apportées aux propriétés du message actif.</span><span class="sxs-lookup"><span data-stu-id="34463-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="34463-114">Pour plus d'informations sur la perspective d'un objet de formulaire dans une application cliente, consultez la rubrique [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="34463-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34463-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34463-115">See also</span></span>



[<span data-ttu-id="34463-116">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="34463-116">MAPI Forms</span></span>](mapi-forms.md)

