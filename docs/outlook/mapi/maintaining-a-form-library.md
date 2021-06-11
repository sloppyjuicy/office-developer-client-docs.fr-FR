---
title: Maintenance d’une bibliothèque de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408802"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="5d10e-103">Maintenance d’une bibliothèque de formulaires</span><span class="sxs-lookup"><span data-stu-id="5d10e-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="5d10e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d10e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d10e-105">Une bibliothèque de formulaires contient toutes les informations importantes sur un formulaire : ses propriétés, ses verbes et les fichiers exécutables de son serveur.</span><span class="sxs-lookup"><span data-stu-id="5d10e-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="5d10e-106">Certains clients permettent à leurs utilisateurs de gérer, d’installer ou de supprimer des serveurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="5d10e-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="5d10e-107">Si vous souhaitez proposer cette fonctionnalité à vos utilisateurs, vous devez avoir accès à :</span><span class="sxs-lookup"><span data-stu-id="5d10e-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="5d10e-108">Fichier de configuration du serveur de formulaire, un fichier avec le . Extension CFG.</span><span class="sxs-lookup"><span data-stu-id="5d10e-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="5d10e-109">Objet conteneur de la bibliothèque de formulaires, objet qui implémente l’interface [IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="5d10e-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="5d10e-110">Pour accéder au fichier de configuration ou à un chemin d’accès, utilisez n’importe quel moyen pratique.</span><span class="sxs-lookup"><span data-stu-id="5d10e-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="5d10e-111">En règle générale, les clients présentent à l’utilisateur une boîte de dialogue pour installer et supprimer des serveurs de formulaires qui peuvent également être utilisés pour demander à l’utilisateur l’emplacement du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="5d10e-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="5d10e-112">Pour accéder au conteneur de la bibliothèque de formulaires, appelez la méthode [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) du gestionnaire de formulaires.</span><span class="sxs-lookup"><span data-stu-id="5d10e-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="5d10e-113">Passez une valeur d’éumération pour spécifier la bibliothèque de formulaires à ouvrir et, si nécessaire, un pointeur vers l’objet que le gestionnaire de formulaires doit utiliser pour ouvrir la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="5d10e-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="5d10e-114">Par exemple, si vous ouvrent une bibliothèque de formulaires de [dossiers,](folder-form-libraries.md)passez un pointeur [IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="5d10e-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="5d10e-115">Après **qu’OpenFormContainer** renvoie le pointeur **IMAPIFormContainer,** appelez [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm,](imapiformcontainer-removeform.md)en fonction de la maintenance à effectuer.</span><span class="sxs-lookup"><span data-stu-id="5d10e-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="5d10e-116">**InstallForm ajoute** un serveur de formulaire à la bibliothèque . **RemoveForm supprime** un serveur de formulaires de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="5d10e-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

