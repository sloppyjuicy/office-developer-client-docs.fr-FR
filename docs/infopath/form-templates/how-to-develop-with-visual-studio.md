---
title: Développement avec Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Vous pouvez grandement améliorer la fonctionnalité de vos formulaires InfoPath en les étendant avec du code managé développé dans Visual Studio 2012. Vous pouvez ensuite publier vos formulaires avec du code pour créer des bibliothèques sur SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300286"
---
# <a name="develop-with-visual-studio"></a>Développement avec Visual Studio

Vous pouvez grandement améliorer la fonctionnalité de vos formulaires InfoPath en les étendant avec du code managé développé dans Visual Studio 2012. Vous pouvez ensuite publier vos formulaires avec du code pour créer des bibliothèques sur SharePoint Server 2013.
  
Vous pouvez commencer à programmer et à développer vos formulaires InfoPath avec code managé en suivant trois étapes importantes :
  
1. Installez Visual Studio 2012 avec le complément [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) . 
    
2. Définissez votre langage de programmation, puis écrivez et déboguez du code dans l'éditeur de code Visual Studio 2012.
    
3. Lorsque vous avez terminé de concevoir le formulaire et de développer votre code, le modèle de formulaire peut être publié sur SharePoint Server 2013.
    
Voici quelques raisons de penser à créer des formulaires compatibles avec SharePoint Server 2013:
  
- Les formulaires déployés sur SharePoint Server 2013 avec InfoPath Forms Services peuvent être remplis dans un navigateur. Cela permet aux utilisateurs qui ne disposent pas d'InfoPath d'ouvrir et d'utiliser vos formulaires.
    
- Vous ne concevez qu'une seule version du formulaire. Les formulaires compatibles avec Microsoft SharePoint Server sont également compatibles avec le caractère de remplissage InfoPath, mais vous ne pouvez pas ouvrir les formulaires compatibles uniquement avec le caractère de remplissage InfoPath dans le navigateur.
    
Il existe deux méthodes pour publier votre formulaire sur SharePoint : SharePoint solutions bac à sable et les solutions déployées par un administrateur. Pour plus d'informations sur chaque méthode de publication et des suggestions sur la méthode la mieux adaptée à votre scénario, voir [publication de formulaires avec code](publishing-forms-with-code.md). Pour obtenir des solutions pour les solutions en bac à sable (sandbox), voir [exemples de solutions en bac à sable](sample-sandboxed-solutions.md).
  
## <a name="developing-with-visual-studio"></a>Développement avec Visual Studio

Avec Visual Studio 2012 et le module complémentaire Microsoft Visual Studio Tools for applications 2012 installé, vous êtes prêt à développer des solutions InfoPath avec code managé.
  
### <a name="choosing-a-programming-language"></a>Sélection d'un langage de programmation

InfoPath fournit les options permettant de programmer à l'aide de quatre versions du modèle objet InfoPath en deux langues: Visual Basic et C#. Les quatre versions du modèle objet sont compatibles avec InfoPath 2013, InfoPath, Office InfoPath 2007 et Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>Pour spécifier le langage de programmation et le modèle objet

1. Ouvrez un projet de modèle de formulaire dans le concepteur InfoPath, cliquez sur **Langage** dans l'onglet **Développeur**. 
    
2. Dans la catégorie **Programmation** de la boîte de dialogue **Options de formulaire**, sélectionnez le langage que vous voulez utiliser dans la liste déroulante **Langage de code du modèle de formulaire**. Ensuite, sélectionnez la version du modèle objet dans la liste déroulante **version cible** . L'option de **version cible** compatible uniquement avec InfoPath 2013 ne dispose pas d'une année de version après le nom d' **InfoPath** . 
    
    > [!NOTE]
    > Not all form template types support code. For example, the **SharePoint List** form template type and **Template Parts** do not support form code. When designing a form template type that does not support code, the **Developer** tab will not be available. De même, seuls certains types de modèles de formulaire prennent en charge les quatre versions du modèle objet. Par exemple, le type de modèle **formulaire vierge (InfoPath Filler)** prend en charge les quatre versions du modèle objet (et crée un modèle de formulaire qui est compatible uniquement avec InfoPath Filler dans ces versions), mais le modèle de **formulaire vierge** prend en charge uniquement InfoPath 2013 et InfoPath (et crée des modèles de formulaires compatibles avec InfoPath Filler et le navigateur). 
  
    Vous pouvez définir un langage de programmation par défaut afin que le concepteur de formulaire InfoPath utilise toujours en premier le langage et la version de modèle objet de votre choix.
    
### <a name="to-set-the-default-programming-language"></a>Pour définir un langage de programmation par défaut

1. Cliquez sur l'onglet **Fichier** et sur **Options**.
    
2. Dans la section **Général** de la boîte de dialogue **Options InfoPath**, cliquez sur **Autres options**.
    
3. Dans l'onglet **Conception** de la boîte de dialogue **Options**, sélectionnez le langage de programmation par défaut à la section **Paramètres de programmation par défaut**. 
    
### <a name="writing-code"></a>Écriture de code

Vous pouvez commencer à développer avec InfoPath 2013 et Visual Studio 2012. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Pour démarrer l'éditeur de code Visual Studio

1. Ouvrez un modèle de formulaire dans le concepteur InfoPath.
    
2. Cliquez sur l' **éditeur de code** dans l'onglet **Développeur**. 
    
> [!TIP]
> Vous pouvez également démarrer l'éditeur de code et ajouter automatiquement des gestionnaires d'événements pour les événements de formulaire et de contrôle à l'aide de commandes de l'onglet **développeur** , des menus contextuels et d'autres méthodes d'interface utilisateur. Pour plus d'informations, consultez la rubrique [Ajouter un gestionnaire d'événements](how-to-add-an-event-handler.md)
  

