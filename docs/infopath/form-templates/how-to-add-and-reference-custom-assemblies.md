---
title: Ajouter et référencer des assemblys personnalisés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using custom assemblies,assemblies [InfoPath 2007], adding custom using InfoPath 2003 object model
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Lorsque vous ajoutez une référence à un assembly personnalisé dans un projet de modèle de formulaire avec code managé , cet assembly est inclus dans le fichier de modèle de formulaire (.xsn) lors de la compilation et de la publication du projet.
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782353"
---
# <a name="add-and-reference-custom-assemblies"></a><span data-ttu-id="cb541-104">Ajouter et référencer des assemblys personnalisés</span><span class="sxs-lookup"><span data-stu-id="cb541-104">Add and Reference Custom Assemblies</span></span>

<span data-ttu-id="cb541-105">Lorsque vous ajoutez une référence à un assembly personnalisé dans un projet de modèle de formulaire avec code managé , cet assembly est inclus dans le fichier de modèle de formulaire (.xsn) lors de la compilation et de la publication du projet.</span><span class="sxs-lookup"><span data-stu-id="cb541-105">When you add a reference to a custom assembly in a managed-code form template project, that assembly is included within the form template file (.xsn) when your project is compiled and published.</span></span>
  
## <a name="add-and-reference-a-custom-assembly"></a><span data-ttu-id="cb541-106">Ajout et référence à un assembly personnalisé</span><span class="sxs-lookup"><span data-stu-id="cb541-106">Add and Reference a Custom Assembly</span></span>

<span data-ttu-id="cb541-p101">Pour éviter un conflit avec la manière dont le projet InfoPath gère les fichiers ajoutés au fichier de modèle du formulaire, ne copiez aucun des assemblys que vous souhaitez référencer dans le dossier du niveau le plus élevé du projet de modèle de formulaire. Par défaut, le chemin est au format < *lecteur*  >:\Utilisateurs\  *NomUtilisateur*  \Documents\Projets InfoPath\  *NomProjet*</span><span class="sxs-lookup"><span data-stu-id="cb541-p101">To avoid a conflict with how the InfoPath project system manages files that are added to the form template file, do not copy any custom assemblies that you want to reference into the top-level folder of a form template project. By default, this will be a path in the following format: < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*</span></span> 
  
<span data-ttu-id="cb541-p102">Si vous souhaitez déplacer des assemblys personnalisés auxquels vous faites référence depuis le dossier du projet, vous devez créer un sous-dossier dans le dossier principal du projet, puis copier et référencer les assemblys personnalisés depuis ce dossier. Cependant, la création d'un sous-dossier pour les assemblys référencés n'est pas nécessaire. Tant qu'un assembly référencé ne se trouve pas dans le dossier de niveau supérieur du projet, le projet InfoPath copie l'assembly dans le fichier de modèle de formulaire (.xsn) lorsque le projet est compilé et publié.</span><span class="sxs-lookup"><span data-stu-id="cb541-p102">If you do want to move custom assemblies that you reference to a location within the project folder, you must create a subfolder under the main project folder, and then copy and reference custom assemblies from that subfolder. However, be aware that creating a subfolder for referenced assemblies is not necessary. As long as a referenced assembly is not located within the project's top-level folder, the InfoPath project system will copy the assembly into the form template file (.xsn) when the project is compiled and published.</span></span>
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a><span data-ttu-id="cb541-112">Référence à un assembly personnalisé depuis son emplacement par défaut</span><span class="sxs-lookup"><span data-stu-id="cb541-112">Reference a custom assembly from its default location</span></span>

1. <span data-ttu-id="cb541-113">Ouvrez le projet de modèle de formulaire dans Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="cb541-113">Open the form template project in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="cb541-114">Dans le menu **Projet**, cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="cb541-114">On the **Project** menu, click **Add Reference**.</span></span>
    
3. <span data-ttu-id="cb541-115">Cliquez sur l'onglet **Parcourir**, recherchez l'assembly, puis cliquez sur **OK** pour ajouter la référence.</span><span class="sxs-lookup"><span data-stu-id="cb541-115">Click the **Browse** tab, locate and specify the assembly, and then click **OK** to add the reference.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="cb541-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb541-116">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="cb541-117">Tâches</span><span class="sxs-lookup"><span data-stu-id="cb541-117">Tasks</span></span>

[<span data-ttu-id="cb541-118">Créer un modèle de formulaire à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="cb541-118">Create a Form Template Using the InfoPath 2003 Object Model</span></span>](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

