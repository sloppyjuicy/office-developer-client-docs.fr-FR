---
title: Installation d’un formulaire dans une bibliothèque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 54b2dece31937b1ff233d4d1e7d8bbc198bfe118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784328"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="a2f25-103">Installation d’un formulaire dans une bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2f25-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="a2f25-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2f25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2f25-105">Le Gestionnaire de formulaire MAPI par défaut fourni avec le Kit de développement Windows ne fournit pas une interface utilisateur pour l’installation de formulaires dans les différentes bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="a2f25-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="a2f25-106">Pour cette raison, vous devez créer une petite application — ou détaillée du jeu d’instructions, que les utilisateurs peuvent utiliser pour installer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a2f25-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="a2f25-107">Si vous implémentez un programme d’installation, la série d’actions qu’il doit effectuer pour installer un formulaire dans le contenu associé d’un dossier tableau sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a2f25-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="a2f25-108">Appelez la fonction [MAPIOpenFormMgr](mapiopenformmgr.md) pour ouvrir le formulaire gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="a2f25-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="a2f25-109">Utilisez [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour sélectionner et ouvrir le conteneur cible pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a2f25-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="a2f25-110">Utilisez la fonction [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) pour installer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a2f25-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="a2f25-111">Étapes 4 à 6 sont à l’installation dans une bibliothèque de formulaires local :</span><span class="sxs-lookup"><span data-stu-id="a2f25-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="a2f25-112">Copiez tous les fichiers vers l’emplacement approprié sur le disque local, si l’installation est à la bibliothèque de formulaires local sur le poste de travail.</span><span class="sxs-lookup"><span data-stu-id="a2f25-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="a2f25-113">Si nécessaire, modifiez le fichier de configuration de formulaire pour refléter les chemins d’accès actuels des composants.</span><span class="sxs-lookup"><span data-stu-id="a2f25-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="a2f25-114">Le fichier de configuration de formulaire peut contenir des chemins d’accès relatifs, auquel cas cette étape ne peut pas être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a2f25-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="a2f25-115">Effectuez les étapes de l’inscription OLE appropriées pour associer le type de message avec le serveur du formulaire en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="a2f25-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="a2f25-116">Si le formulaire a été installé dans la bibliothèque de formulaires local, copiez icône (.ico) et les fichiers de configuration (.cfg) du formulaire dans le répertoire %WINDOWS%\FORMS\CONFIGS afin que le formulaire peut être restauré automatiquement au cas où la bibliothèque de formulaires est endommagée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="a2f25-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="a2f25-117">Cette étape est recommandée, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a2f25-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a2f25-118">Vous pouvez simplifier l’installation à une bibliothèque de formulaires local en remplaçant les étapes 1 et 2 par un appel à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="a2f25-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2f25-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f25-119">See also</span></span>



[<span data-ttu-id="a2f25-120">Développez serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="a2f25-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

