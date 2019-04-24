---
title: Installation d'un formulaire dans une bibliothèque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317233"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="83dc3-103">Installation d'un formulaire dans une bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83dc3-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="83dc3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83dc3-105">Le gestionnaire de formulaires MAPI par défaut fourni avec le kit de développement logiciel (SDK) Windows ne fournit pas d'interface utilisateur pour l'installation des formulaires dans les différentes bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="83dc3-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="83dc3-106">Pour cette raison, vous devrez créer une petite application, ou un ensemble d'instructions détaillé, que les utilisateurs peuvent utiliser pour installer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="83dc3-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="83dc3-107">Si vous implémentez une application d'installation, la série d'actions qu'elle doit effectuer pour installer un formulaire dans le tableau des contenus associés d'un dossier est la suivante:</span><span class="sxs-lookup"><span data-stu-id="83dc3-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="83dc3-108">Appelez la fonction [MAPIOpenFormMgr](mapiopenformmgr.md) pour ouvrir le gestionnaire de formulaires.</span><span class="sxs-lookup"><span data-stu-id="83dc3-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="83dc3-109">Utilisez [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) méthode pour sélectionner et ouvrir le conteneur cible pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="83dc3-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="83dc3-110">Utilisez la fonction [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) pour installer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="83dc3-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="83dc3-111">Les étapes 4 à 6 concernent l'installation dans une bibliothèque de formulaires locale:</span><span class="sxs-lookup"><span data-stu-id="83dc3-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="83dc3-112">Copiez tous les fichiers à l'emplacement approprié sur le disque local, si l'installation est effectuée vers la bibliothèque de formulaires locale sur la station de travail de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83dc3-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="83dc3-113">Si nécessaire, modifiez le fichier de configuration du formulaire pour refléter les chemins d'accès actuels des composants.</span><span class="sxs-lookup"><span data-stu-id="83dc3-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="83dc3-114">Le fichier de configuration de formulaire peut contenir des chemins d'accès relatifs, auquel cas cette étape n'est peut-être pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="83dc3-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="83dc3-115">Suivez les étapes d'enregistrement OLE appropriées pour associer le type de message au serveur de formulaires en cours d'installation.</span><span class="sxs-lookup"><span data-stu-id="83dc3-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="83dc3-116">Si le formulaire a été installé dans la bibliothèque de formulaires locale, copiez les fichiers icône (. ico) et de configuration (. cfg) du formulaire dans le répertoire%WINDOWS%\FORMS\CONFIGS afin que le formulaire puisse être restauré automatiquement si la bibliothèque de formulaires est endommagée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="83dc3-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="83dc3-117">Cette étape est recommandée, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="83dc3-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="83dc3-118">Vous pouvez simplifier l'installation dans une bibliothèque de formulaires locale en remplaçant les étapes 1 et 2 par un appel à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="83dc3-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83dc3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83dc3-119">See also</span></span>



[<span data-ttu-id="83dc3-120">Développement de serveurs de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="83dc3-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

