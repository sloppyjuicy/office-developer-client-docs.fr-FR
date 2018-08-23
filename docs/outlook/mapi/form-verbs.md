---
title: Formulaire verbes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 27999c141fdeb3e1610213db128bc4ad3d049e6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594102"
---
# <a name="form-verbs"></a><span data-ttu-id="5ab8a-103">Formulaire verbes</span><span class="sxs-lookup"><span data-stu-id="5ab8a-103">Form verbs</span></span>

<span data-ttu-id="5ab8a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ab8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ab8a-105">Interface utilisateur d’un formulaire offre généralement des éléments de menu ou des contrôles permettant aux utilisateurs d’effectuer un type d’action avec le formulaire.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="5ab8a-106">Il est le travail du serveur de formulaire pour gérer ces actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="5ab8a-107">Cette interface est implémentée à l’aide des API Win32 standard ; une écriture est tout simplement à rédiger des autres interfaces pour les programmes Win32 régulières.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="5ab8a-108">Souvent, les actions de l’utilisateur sont associées à des verbes.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="5ab8a-109">Un verbe est le nom d’une action qui est spécifique à une certaine classe de message.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="5ab8a-110">Par exemple, la **réponse** est un verbe qui est implémenté par de nombreux serveurs de formulaire, chacun d'entre eux peut avoir une autre interprétation de ce verbe.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="5ab8a-111">Verbes sont parfois en tant que commandes.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5ab8a-112">Pas tous les éléments de menu et les contrôles d’un formulaire correspondent à un verbe.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="5ab8a-113">Par exemple, un bouton **Annuler** ne correspond pas à un verbe Cancel sur le serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="5ab8a-114">En règle générale, les verbes sont associés à des actions qui sont spécifiques à une classe de message spécifique ou un ensemble de classes de message.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="5ab8a-115">Bien que les différentes classes de messages peuvent prendre en charge plusieurs ensembles de verbes, tous les prend en charge au moins le verbe Open, qui affiche l’interface utilisateur du formulaire et la charge de valeurs de propriété du message.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="5ab8a-116">Verbes ne peuvent prendre aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-116">Verbs may take no parameters.</span></span> <span data-ttu-id="5ab8a-117">Formulaires exporter des commandes à l’aide des paramètres variables doivent utiliser les mécanismes d’Automation.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="5ab8a-118">Les clients peuvent déterminer les verbes sont pris en charge par une classe de message spécifique par le biais de la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , qui est implémentée par le Gestionnaire de formulaire MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="5ab8a-119">Le Gestionnaire de formulaire obtient ces informations à partir du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="5ab8a-120">Le jeu de verbe renvoyé par cette méthode est utilisé par le client pour afficher les commandes pouvant être exécutées sur un message.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="5ab8a-121">Par exemple, un client peut activer les utilisateurs à cliquer sur le bouton droit de la souris sur un message à afficher les verbes applicables à ce message.</span><span class="sxs-lookup"><span data-stu-id="5ab8a-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ab8a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ab8a-122">See also</span></span>

- [<span data-ttu-id="5ab8a-123">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab8a-123">MAPI Forms</span></span>](mapi-forms.md)

