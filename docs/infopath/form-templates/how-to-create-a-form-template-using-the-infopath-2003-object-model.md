---
title: Créer un modèle de formulaire à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2007, creating InfoPath 2003-compatible form templates
ms.localizationpriority: medium
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: Les procédures de cette rubrique expliquent comment créer un modèle de formulaire qui fonctionne avec le modèle objet compatible InfoPath 2003.
ms.openlocfilehash: 73d14eb493f063bfbfe292bc2b43be81585fe79d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621226"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a>Créer un modèle de formulaire à l’aide du modèle objet InfoPath 2003

Les procédures de cette rubrique expliquent comment créer un modèle de formulaire qui fonctionne avec le modèle objet compatible InfoPath 2003.
  
> [!IMPORTANT]
> In addition to the procedures below, you must also click the **File** tab, click **Save As**, and then select **InfoPath 2003 Form Template** in the **Save as type** box to save the form template to the InfoPath 2003-compatible file format. Also, to open InfoPath 2003-compatible form templates created with InfoPath, all InfoPath 2003 users must have the .NET Framework 2.0 or later installed on their computers. 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a>Pour créer un modèle de formulaire compatible InfoPath 2003 dans InfoPath avec Visual Studio Tools for Applications

1. Démarrez le Concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire**.
    
3. Dans la catégorie **Compatibilité**, sélectionnez **Formulaire InfoPath 2003**.
    
4. Dans la catégorie **Programmation**, sélectionnez **C# (compatible avec InfoPath 2003)** ou **Visual Basic (compatible avec InfoPath 2003)** dans la liste déroulante **Langage du code du modèle de formulaire**. 
    
5. Cliquez sur **OK**.
    
6. Concevez votre modèle de formulaire, puis ajoutez des handlers d’événements dans Visual Studio 2012, comme décrit dans Ajouter un handler d’événements à l’aide du modèle objet [InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
    
## <a name="see-also"></a>Voir aussi



[Procédure pas à pas : Création et débogage d'un modèle de formulaire basique à l'aide du modèle objet InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)
  
[Création de modèles de formulaires à l’aide du modèle objet InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)

