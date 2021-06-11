---
title: Verbes de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424027"
---
# <a name="form-verbs"></a><span data-ttu-id="6b17b-103">Verbes de formulaires</span><span class="sxs-lookup"><span data-stu-id="6b17b-103">Form verbs</span></span>

<span data-ttu-id="6b17b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b17b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b17b-105">L’interface utilisateur d’un formulaire propose généralement des éléments de menu ou des contrôles qui permettent aux utilisateurs d’agir sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6b17b-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="6b17b-106">Le rôle du serveur de formulaires est de gérer ces actions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b17b-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="6b17b-107">Cette interface est implémentée à l’aide des API Win32 standard ; L’écriture d’une interface est tout comme l’écriture d’autres interfaces pour des programmes Win32 ordinaires.</span><span class="sxs-lookup"><span data-stu-id="6b17b-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="6b17b-108">Souvent, les actions de l’utilisateur sont associées à des verbes.</span><span class="sxs-lookup"><span data-stu-id="6b17b-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="6b17b-109">Un verbe est le nom d’une action spécifique à une classe de message spécifique.</span><span class="sxs-lookup"><span data-stu-id="6b17b-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="6b17b-110">Par exemple, **Reply** est un verbe implémenté par de nombreux serveurs de formulaires, chacun d’eux peut avoir une interprétation différente de ce verbe.</span><span class="sxs-lookup"><span data-stu-id="6b17b-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="6b17b-111">Les verbes sont parfois appelés commandes.</span><span class="sxs-lookup"><span data-stu-id="6b17b-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6b17b-112">Certains éléments de menu et contrôles d’un formulaire ne correspondent pas à un verbe.</span><span class="sxs-lookup"><span data-stu-id="6b17b-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="6b17b-113">Par exemple, un **bouton Annuler** ne correspond pas à un verbe Cancel dans le serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="6b17b-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="6b17b-114">En règle générale, les verbes sont associés à des actions spécifiques à une classe de message particulière ou à un ensemble de classes de message.</span><span class="sxs-lookup"><span data-stu-id="6b17b-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="6b17b-115">Bien que différentes classes de messages peuvent prendre en charge différents ensembles de verbes, toutes la prise en charge au moins le verbe Ouvrir, qui affiche l’interface utilisateur du formulaire et le charge avec les valeurs de propriété du message.</span><span class="sxs-lookup"><span data-stu-id="6b17b-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="6b17b-116">Les verbes ne prennent aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6b17b-116">Verbs may take no parameters.</span></span> <span data-ttu-id="6b17b-117">Les formulaires qui exportent des commandes avec des paramètres variables doivent utiliser les mécanismes Automation.</span><span class="sxs-lookup"><span data-stu-id="6b17b-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="6b17b-118">Les clients peuvent déterminer les verbes pris en charge par une classe de message particulière via la méthode [IMAPIFormInfo::CalcVerbSet,](imapiforminfo-calcverbset.md) qui est implémentée par le gestionnaire de formulaire MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b17b-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="6b17b-119">Le gestionnaire de formulaire obtient ces informations à partir du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6b17b-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="6b17b-120">Le verbe renvoyé par cette méthode est utilisé par le client pour afficher à l’utilisateur les commandes qui peuvent être exécutées sur un message.</span><span class="sxs-lookup"><span data-stu-id="6b17b-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="6b17b-121">Par exemple, un client peut permettre aux utilisateurs de cliquer sur le bouton droit de la souris sur un message pour afficher les verbes applicables à ce message.</span><span class="sxs-lookup"><span data-stu-id="6b17b-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b17b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b17b-122">See also</span></span>

- [<span data-ttu-id="6b17b-123">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="6b17b-123">MAPI Forms</span></span>](mapi-forms.md)

