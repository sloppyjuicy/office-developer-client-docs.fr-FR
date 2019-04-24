---
title: Accéder aux données de l'application
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- application names [infopath 2007],accessing application name [InfoPath 2007],InfoPath 2007, accessing application data,accessing application version [InfoPath 2007],application versions [InfoPath 2007],language IDs [InfoPath 2007],LCID [InfoPath 2007],application data [InfoPath 2007],accessing language ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Le modèle objet InfoPath avec code managé fournit des objets et des collections qui peuvent être utilisés pour accéder aux informations sur l'application InfoPath, y compris celles associées au document XML sous-jacent d'un formulaire et au fichier de définition de formulaire (.xsf). Ces données sont accessibles à travers l'objet de niveau supérieur dans la hiérarchie des modèles d'objets InfoPath qui est instanciée à l'aide de la classe Application .
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300174"
---
# <a name="access-application-data"></a>Accéder aux données de l'application

Le modèle objet InfoPath avec code managé fournit des objets et des collections qui peuvent être utilisés pour accéder aux informations sur l'application InfoPath, y compris celles associées au document XML sous-jacent d'un formulaire et au fichier de définition de formulaire (.xsf). Ces données sont accessibles à travers l'objet de niveau supérieur dans la hiérarchie des modèles d'objets InfoPath qui est instanciée à l'aide de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
Dans un projet de modèle de formulaire InfoPath avec code managé, créé à l'aide de Visual Studio 2012, vous pouvez utiliser le mot clé **this** (C#) ou **Me** (Visual Basic) pour accéder à une instance de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) qui représente l'application InfoPath actuelle pouvant être utilisée pour accéder aux propriétés et aux méthodes de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
## <a name="example"></a>Exemple

### <a name="displaying-the-application-name-version-and-language-id"></a>Affichage du nom de l'application, de la version et de l'identificateur de langue

Dans l'exemple suivant, les propriétés [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) et [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) permettent de renvoyer le nom et le numéro de version de l'instance InfoPath. La propriété [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) est ensuite utilisée pour renvoyer un objet **LanguageSettings** qui à son tour permet de renvoyer le code LCID (nombre de quatre chiffres) de la langue actuellement utilisée pour l'interface utilisateur InfoPath. Enfin, toutes ces informations sont affichées dans une zone de message. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Pour que la propriété **LanguageSettings** fonctionne, vous devez établir une référence à la bibliothèque d'objets Microsoft Office 14.0 (sous l'onglet **COM** de la boîte de dialogue **Ajouter une référence** dans Visual Studio 2012). Cette opération établit une référence à l'espace de noms **Microsoft.Office.Core**, qui contient la classe **LanguageSettings**. En outre, le formulaire doit être exécuté au niveau Confiance totale. 
  
Cet exemple a besoin d'une directive **using** ou **Imports** pour l'espace de noms **Microsoft.Office.Core** dans la section des déclarations du module de code du formulaire. 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


