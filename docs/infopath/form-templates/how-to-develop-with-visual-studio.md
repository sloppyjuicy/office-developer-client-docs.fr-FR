---
title: Développement avec Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Vous pouvez facilement améliorer les fonctionnalités de vos formulaires InfoPath en les étendant avec du code managé dans Visual Studio 2012. Vous pouvez publier vos formulaires avec code aux bibliothèques de formulaires dans SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401096"
---
# <a name="develop-with-visual-studio"></a>Développement avec Visual Studio

Vous pouvez facilement améliorer les fonctionnalités de vos formulaires InfoPath en les étendant avec du code managé dans Visual Studio 2012. Vous pouvez publier vos formulaires avec code aux bibliothèques de formulaires dans SharePoint Server 2013.
  
Vous pouvez commencer à programmer et à développer vos formulaires InfoPath avec code managé en suivant trois étapes importantes :
  
1. Installez Visual Studio 2012 avec le module complémentaire [Microsoft Visual Studio Tools pour Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) . 
    
2. Définissez votre langage de programmation, puis écrire et déboguer le code dans l’éditeur de code Visual Studio 2012.
    
3. Lorsque vous avez terminé la conception du formulaire et du développement de votre code, le modèle de formulaire peut être publié sur SharePoint Server 2013.
    
Voici quelques raisons d’utiliser la création de formulaires compatibles avec SharePoint Server 2013 :
  
- Déployé vers SharePoint Server 2013 avec InfoPath Forms Services peuvent remplir les formulaires dans un navigateur. Cela permet aux utilisateurs qui n’ont pas installé pour ouvrir et utiliser vos formulaires InfoPath.
    
- Vous ne concevez qu’une seule version du formulaire. Les formulaires compatibles avec Microsoft SharePoint Server sont également compatibles avec le caractère de remplissage InfoPath, mais vous ne pouvez pas ouvrir les formulaires compatibles uniquement avec le caractère de remplissage InfoPath dans le navigateur.
    
Il existe deux méthodes pour publier votre formulaire sur SharePoint : SharePoint solutions bac à sable et les solutions déployées par un administrateur. Pour plus d’informations sur chaque méthode de publication et des suggestions sur laquelle la méthode est recommandée pour votre scénario, voir [Publishing Forms with Code](publishing-forms-with-code.md). Par exemple, les solutions pour les solutions en bac à sable, voir [Exemples de Solutions en bac à sable](sample-sandboxed-solutions.md).
  
## <a name="developing-with-visual-studio"></a>Développement avec Visual Studio

Avec Visual Studio 2012 et Microsoft Visual Studio Tools pour le module complémentaire 2012 Applications installé, vous êtes prêt à commencer à développer des solutions de code managé de InfoPath.
  
### <a name="choosing-a-programming-language"></a>Sélection d'un langage de programmation

InfoPath fournit les options pour programmer à l’aide de quatre versions du modèle objet InfoPath dans deux langages : Visual Basic et Visual C#. Les quatre versions du modèle objet assurent la compatibilité avec InfoPath 2013, InfoPath, Microsoft Office InfoPath 2007 et Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>Pour spécifier le langage de programmation et le modèle objet

1. Ouvrez un projet de modèle de formulaire dans le concepteur InfoPath, cliquez sur **Langage** dans l'onglet **Développeur**. 
    
2. Dans la catégorie **Programmation** de la boîte de dialogue **Options de formulaire**, sélectionnez le langage que vous voulez utiliser dans la liste déroulante **Langage de code du modèle de formulaire**. Ensuite, sélectionnez la version du modèle objet à partir de la liste déroulante **version cible** . L’option **version cible** qui est compatible uniquement avec InfoPath 2013 ne dispose pas d’une année de version suit le nom **d’InfoPath** . 
    
    > [!NOTE]
    > Pas tous les types de modèle de formulaire prennent en charge le code. Par exemple, le type de modèle de formulaire de **Liste SharePoint** et **Composants de modèle** ne prennent pas en charge le code du formulaire. Lorsque vous créez un type de modèle de formulaire qui ne prend pas en charge le code, l’onglet **développeur** ne sera pas disponible. En outre, seuls certains types de modèle de formulaire prennent en charge toutes les versions de quatre du modèle objet. Par exemple, le type de modèle de **Formulaire vierge (InfoPath Filler)** prend en charge toutes les versions de quatre du modèle d’objet (et crée le modèle de formulaire qui sont uniquement compatibles avec InfoPath Filler dans ces versions), mais le modèle de **Formulaire vierge** prend uniquement en charge 2013 InfoPath et InfoPath (et crée des modèles de formulaires compatibles avec InfoPath Filler et le navigateur). 
  
    Vous pouvez définir un langage de programmation par défaut afin que le concepteur de formulaire InfoPath utilise toujours en premier le langage et la version de modèle objet de votre choix.
    
### <a name="to-set-the-default-programming-language"></a>Pour définir un langage de programmation par défaut

1. Cliquez sur l'onglet **Fichier** et sur **Options**.
    
2. Dans la section **Général** de la boîte de dialogue **Options InfoPath**, cliquez sur **Autres options**.
    
3. Dans l'onglet **Conception** de la boîte de dialogue **Options**, sélectionnez le langage de programmation par défaut à la section **Paramètres de programmation par défaut**. 
    
### <a name="writing-code"></a>Écriture de Code

Vous pouvez maintenant commencer à développer avec InfoPath 2013 et Visual Studio 2012. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Pour démarrer l’éditeur de Code Visual Studio

1. Ouvrez un modèle de formulaire dans le concepteur InfoPath.
    
2. Cliquez sur l' **éditeur de code** dans l'onglet **Développeur**. 
    
> [!TIP]
> Vous pouvez également démarrer l’éditeur de code et ajouter automatiquement des gestionnaires d’événements pour les événements de formulaire et du contrôle à l’aide de commandes sur l’onglet **développeur** , les menus contextuels et les autres méthodes d’interface utilisateur. Pour plus d’informations, voir [Ajouter un gestionnaire d’événements](how-to-add-an-event-handler.md)
  

