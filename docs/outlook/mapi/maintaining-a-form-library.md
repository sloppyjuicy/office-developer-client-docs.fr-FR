---
title: Maintenance d’une bibliothèque de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784538"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="49257-103">Maintenance d’une bibliothèque de formulaires</span><span class="sxs-lookup"><span data-stu-id="49257-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="49257-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49257-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49257-105">Une bibliothèque de formulaires conserve toutes les informations importantes sur un formulaire : ses propriétés, ses verbes et les fichiers exécutables de son serveur.</span><span class="sxs-lookup"><span data-stu-id="49257-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="49257-106">Certains clients permettent à leurs utilisateurs à mettre à jour, installer ou supprimer des serveurs de formulaire.</span><span class="sxs-lookup"><span data-stu-id="49257-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="49257-107">Si vous souhaitez offrir cette fonctionnalité à vos utilisateurs, vous devez avoir accès à :</span><span class="sxs-lookup"><span data-stu-id="49257-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="49257-108">Fichier de configuration du serveur de formulaire, un fichier avec le. Extension CFG.</span><span class="sxs-lookup"><span data-stu-id="49257-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="49257-109">Objet de conteneur de la bibliothèque de formulaires, un objet qui implémente le [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="49257-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="49257-110">Pour accéder au fichier de configuration ou un chemin d’accès à celui-ci, utilisez procédé conviennent.</span><span class="sxs-lookup"><span data-stu-id="49257-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="49257-111">En règle générale, les clients présenter l’utilisateur avec une boîte de dialogue pour l’installation et la suppression de serveurs de formulaire qui peuvent également être utilisées pour inviter l’utilisateur à l’emplacement du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="49257-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="49257-112">Pour accéder au conteneur de la bibliothèque de formulaires, appelez la méthode de [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) de responsable de l’écran.</span><span class="sxs-lookup"><span data-stu-id="49257-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="49257-113">Transmettez une valeur d’énumération pour spécifier la bibliothèque formulaire à ouvrir et si nécessaire, un pointeur vers l’objet du Gestionnaire de formulaire à utiliser pour ouvrir la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="49257-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="49257-114">Par exemple, si vous ouvrez un [Dossier les bibliothèques de formulaires](folder-form-libraries.md), passez un [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointeur.</span><span class="sxs-lookup"><span data-stu-id="49257-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="49257-115">Une fois que **OpenFormContainer** renvoie le pointeur **IMAPIFormContainer** , appelez [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), en fonction de la maintenance à effectuer.</span><span class="sxs-lookup"><span data-stu-id="49257-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="49257-116">**InstallForm** ajoute un serveur de formulaire à la bibliothèque ; **RemoveForm** supprime un serveur de formulaire de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="49257-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

