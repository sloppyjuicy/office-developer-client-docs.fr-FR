---
title: Création d'un contrôle ActiveX pouvant lier des données de formulaire InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Vous pouvez héberger des contrôles ActiveX dans les formulaires InfoPath qui sont conçus pour être ouverts dans l'éditeur InfoPath. Ces contrôles peuvent être créés au préalable (avec certaines contraintes) ou ils peuvent être écrits spécialement pour InfoPath.
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782348"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Création d'un contrôle ActiveX pouvant lier des données de formulaire InfoPath

Vous pouvez héberger des contrôles ActiveX dans les formulaires InfoPath qui sont conçus pour être ouverts dans l'éditeur InfoPath. Ces contrôles peuvent être créés au préalable (avec certaines contraintes) ou ils peuvent être écrits spécialement pour InfoPath.
  
## <a name="write-an-activex-control"></a>Création d'un contrôle ActiveX

De même que les autres contrôles de InfoPath, les contrôles ActiveX doivent prendre en charge des interfaces COM existantes :
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Afin que InfoPath mette à jour des propriétés du modèle objet de document (DOM, Document Object Model) au moment où ils changent dans le contrôle, le contrôle doit implémenter les interfaces ci-après.
  
- **IConnectionPointContainer**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
De plus, il existe deux interfaces COM propres à InfoPath qui fournissent une meilleure intégration des contrôles :
  
- [IInfoPathControl](http://msdn.microsoft.com/en-us/library/bb264625.aspx)
    
- [IInfoPathControlSite](http://msdn.microsoft.com/en-us/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Ajout d'un contrôle ActiveX à l'environnement de création InfoPath

La commande **Ajouter ou supprimer des contrôles personnalisés** dans le volet de tâches **Contrôles** vous permet d'utiliser l' **Assistant Ajout de contrôle personnalisé** pour ajouter un contrôle personnalisé. En utilisant l'assistant, vous pouvez sélectionner un contrôle ActiveX déjà enregistré ou rechercher des contrôles personnalisés supplémentaires sur Office Marketplace. Après avoir sélectionné un contrôle, vous pouvez spécifier les éléments ci-après. 
  
- Spécifiez un CAB pour installer le contrôle ActiveX avec votre modèle de formulaire.
    
- Spécifiez une propriété de liaison pour lier à XML.
    
- Spécifiez une propriété utilisée pour activer ou désactiver le contrôle en fonction de règles ou de signatures numériques. Cela peut être utile, notamment, lorsque XML n'est pas présent ou qu'une mise en forme conditionnelle est utilisée.
    
- Spécifiez la liaison du type de données.
    
> [!NOTE]
> [!REMARQUE] Si vous développez un contrôle ActiveX et l'ajoutez au volet de tâches **Contrôles** de InfoPath, vous ne pouvez pas le recréer tant que InfoPath n'est pas fermé. 
  
## <a name="deploy-an-activex-control"></a>Déploiement d'un contrôle ActiveX

Pour distribuer un contrôle ActiveX, vous pouvez écrire un programme d'installation qui installe le contrôle sur l'ordinateur cible et copie le fichier de modèle de contrôle (ICT) InfoPath et le fichier CAB dans le dossier de l'utilisateur, \Users\\<nom d'utilisateur\>\AppData\Local\Microsoft\InfoPath\Controls. Notez que si deux développeurs ou plus participent au développement de formulaires utilisant des contrôles ActiveX, chaque développeur doit disposer des contrôles ajoutés à l'environnement de création InfoPath, sinon il ne peut pas modifier les propriétés des contrôles de InfoPath.
  
## <a name="see-also"></a>Voir aussi



Atelier 6 : Ajout de contrôles ActiveX dans InfoPath 2003
  
[Création d'un contrôle InfoPath personnalisé à l'aide de C# et .NET (blog de l'équipe InfoPath) (éventuellement en anglais)](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)

