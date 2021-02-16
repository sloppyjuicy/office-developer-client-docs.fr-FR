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
ms.openlocfilehash: 19b5f06231bb03cfac8b32b157e03956b5fc334e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431168"
---
# <a name="add-and-reference-custom-assemblies"></a>Ajouter et référencer des assemblys personnalisés

Lorsque vous ajoutez une référence à un assembly personnalisé dans un projet de modèle de formulaire avec code managé
, cet assembly est inclus dans le fichier de modèle de formulaire (.xsn) lors de la compilation et de la publication du projet.
  
## <a name="add-and-reference-a-custom-assembly"></a>Ajout et référence à un assembly personnalisé

Pour éviter un conflit avec la manière dont le projet InfoPath gère les fichiers ajoutés au fichier de modèle du formulaire, ne copiez aucun des assemblys que vous souhaitez référencer dans le dossier du niveau le plus élevé du projet de modèle de formulaire. Par défaut, le chemin est au format < *lecteur*  >:\Utilisateurs\  *NomUtilisateur*  \Documents\Projets InfoPath\  *NomProjet* 
  
Si vous souhaitez déplacer des assemblys personnalisés auxquels vous faites référence depuis le dossier du projet, vous devez créer un sous-dossier dans le dossier principal du projet, puis copier et référencer les assemblys personnalisés depuis ce dossier. Cependant, la création d'un sous-dossier pour les assemblys référencés n'est pas nécessaire. Tant qu'un assembly référencé ne se trouve pas dans le dossier de niveau supérieur du projet, le projet InfoPath copie l'assembly dans le fichier de modèle de formulaire (.xsn) lorsque le projet est compilé et publié.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Référence à un assembly personnalisé depuis son emplacement par défaut

1. Ouvrez le projet de modèle de formulaire dans Visual Studio 2012.
    
2. Dans le menu **Projet**, cliquez sur **Ajouter une référence**.
    
3. Cliquez sur l'onglet **Parcourir**, recherchez l'assembly, puis cliquez sur **OK** pour ajouter la référence. 
    
## <a name="see-also"></a>Voir aussi

#### <a name="tasks"></a>Tâches

[Créer un modèle de formulaire à l’aide du modèle objet InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

