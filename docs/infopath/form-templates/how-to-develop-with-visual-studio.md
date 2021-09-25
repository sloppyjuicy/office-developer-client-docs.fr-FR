---
title: Développement avec Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Vous pouvez grandement améliorer les fonctionnalités de vos formulaires InfoPath en les étendant avec du code géré développé dans Visual Studio 2012. Vous pouvez ensuite publier vos formulaires avec du code dans des bibliothèques de formulaires SharePoint Server 2013.
ms.openlocfilehash: b7d2437e671a13ceafc6c11a6dd83d39f8ffa76b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625902"
---
# <a name="develop-with-visual-studio"></a>Développement avec Visual Studio

Vous pouvez grandement améliorer les fonctionnalités de vos formulaires InfoPath en les étendant avec du code géré développé dans Visual Studio 2012. Vous pouvez ensuite publier vos formulaires avec du code dans des bibliothèques de formulaires SharePoint Server 2013.
  
Vous pouvez commencer à programmer et à développer vos formulaires InfoPath avec code managé en suivant trois étapes importantes :
  
1. Installez Visual Studio 2012 avec [le module Microsoft® Visual Studio® Tools for Applications 2012.](https://www.microsoft.com/en-us/download/details.aspx?id=38807) 
    
2. Définissez votre langage de programmation, puis écrivez et déboguer du code dans l’éditeur de code Visual Studio 2012.
    
3. Lorsque vous avez terminé de concevoir le formulaire et de développer votre code, le modèle de formulaire peut être publié sur SharePoint Server 2013.
    
Voici quelques raisons de créer des formulaires compatibles avec SharePoint Server 2013 :
  
- Les formulaires déployés SharePoint Server 2013 avec InfoPath Forms Services peuvent être remplis dans un navigateur. Cela permet aux utilisateurs qui n’ont pas Installé InfoPath d’ouvrir et d’utiliser vos formulaires.
    
- Vous ne concevez qu’une seule version du formulaire. Les formulaires compatibles avec Microsoft SharePoint Server sont également compatibles avec le caractère de remplissage InfoPath, mais vous ne pouvez pas ouvrir les formulaires compatibles uniquement avec le caractère de remplissage InfoPath dans le navigateur.
    
Il existe deux méthodes pour publier votre formulaire sur SharePoint : SharePoint solutions bac à sable et les solutions déployées par un administrateur. Pour plus d’informations sur chaque méthode de composition et des suggestions sur la méthode la plus efficace pour votre scénario, voir [Publishing Forms with Code](publishing-forms-with-code.md). Pour obtenir des exemples de solutions pour les solutions en bac à sable, voir Exemples de solutions en bac à sable ( [sandbox).](sample-sandboxed-solutions.md)
  
## <a name="developing-with-visual-studio"></a>Développement avec Visual Studio

Avec Visual Studio 2012 et le module complémentaire Microsoft® Visual Studio® Tools for Applications 2012 installés, vous êtes prêt à commencer à développer des solutions InfoPath avec code géré.
  
### <a name="choosing-a-programming-language"></a>Sélection d'un langage de programmation

InfoPath propose des options de programmation à l’aide de quatre versions du modèle objet InfoPath en deux langues : Visual Basic et C#. Les quatre versions du modèle objet assurent la compatibilité avec InfoPath 2013, InfoPath, Office InfoPath 2007 et Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>Pour spécifier le langage de programmation et le modèle objet

1. Ouvrez un projet de modèle de formulaire dans le concepteur InfoPath, cliquez sur **Langage** dans l'onglet **Développeur**. 
    
2. Dans la catégorie **Programmation** de la boîte de dialogue **Options de formulaire**, sélectionnez le langage que vous voulez utiliser dans la liste déroulante **Langage de code du modèle de formulaire**. Ensuite, sélectionnez la version du modèle objet dans la liste de listes de **listes** bas de la version cible. **L’option de version** cible qui est compatible uniquement avec InfoPath 2013 n’a pas d’année de version suivant le nom **InfoPath.** 
    
    > [!NOTE]
    > Not all form template types support code. For example, the **SharePoint List** form template type and **Template Parts** do not support form code. When designing a form template type that does not support code, the **Developer** tab will not be available. En outre, seuls certains types de modèles de formulaires sont en charge dans les quatre versions du modèle objet. Par exemple, le type de modèle Formulaire vide **(InfoPath Filler)** prend en charge les quatre versions du modèle objet  (et crée un modèle de formulaire compatible uniquement avec InfoPath Filler dans ces versions), mais le modèle Formulaire vide prend uniquement en charge InfoPath 2013 et InfoPath (et crée des modèles de formulaire compatibles avec InfoPath Filler et le navigateur). 
  
    Vous pouvez définir un langage de programmation par défaut afin que le concepteur de formulaire InfoPath utilise toujours en premier le langage et la version de modèle objet de votre choix.
    
### <a name="to-set-the-default-programming-language"></a>Pour définir un langage de programmation par défaut

1. Cliquez sur l'onglet **Fichier** et sur **Options**.
    
2. Dans la section **Général** de la boîte de dialogue **Options InfoPath**, cliquez sur **Autres options**.
    
3. Dans l'onglet **Conception** de la boîte de dialogue **Options**, sélectionnez le langage de programmation par défaut à la section **Paramètres de programmation par défaut**. 
    
### <a name="writing-code"></a>Écriture de code

Vous pouvez maintenant commencer à développer avec InfoPath 2013 et Visual Studio 2012. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Pour démarrer l’éditeur Visual Studio Code de publication

1. Ouvrez un modèle de formulaire dans le concepteur InfoPath.
    
2. Cliquez sur l' **éditeur de code** dans l'onglet **Développeur**. 
    
> [!TIP]
> Vous pouvez également démarrer l’éditeur de code et ajouter automatiquement des handlers d’événements pour les événements de formulaire et de contrôle à l’aide des commandes de l’onglet Développeur, des menus contextiels et d’autres méthodes d’interface utilisateur.  Pour plus d’informations, voir [Ajouter un handler d’événements](how-to-add-an-event-handler.md)
  

