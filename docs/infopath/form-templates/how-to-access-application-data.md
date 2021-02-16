---
title: Accéder aux données d’application
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- application names [infopath 2007],accessing application name [InfoPath 2007],InfoPath 2007, accessing application data,accessing application version [InfoPath 2007],application versions [InfoPath 2007],language IDs [InfoPath 2007],LCID [InfoPath 2007],application data [InfoPath 2007],accessing language ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Le modèle objet InfoPath avec code managé fournit des objets et des collections qui peuvent être utilisés pour accéder aux informations sur l'application InfoPath, y compris celles associées au document XML sous-jacent d'un formulaire et au fichier de définition de formulaire (.xsf). Ces données sont accessibles à travers l'objet de niveau supérieur dans la hiérarchie des modèles d'objets InfoPath qui est instanciée à l'aide de la classe Application .
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417230"
---
# <a name="access-application-data"></a><span data-ttu-id="cd8ef-105">Accéder aux données d’application</span><span class="sxs-lookup"><span data-stu-id="cd8ef-105">Access Application Data</span></span>

<span data-ttu-id="cd8ef-p102">Le modèle objet InfoPath avec code managé fournit des objets et des collections qui peuvent être utilisés pour accéder aux informations sur l'application InfoPath, y compris celles associées au document XML sous-jacent d'un formulaire et au fichier de définition de formulaire (.xsf). Ces données sont accessibles à travers l'objet de niveau supérieur dans la hiérarchie des modèles d'objets InfoPath qui est instanciée à l'aide de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cd8ef-p102">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file. This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="cd8ef-108">Dans un projet de modèle de formulaire InfoPath avec code managé, créé à l'aide de Visual Studio 2012, vous pouvez utiliser le mot clé **this** (C#) ou **Me** (Visual Basic) pour accéder à une instance de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) qui représente l'application InfoPath actuelle pouvant être utilisée pour accéder aux propriétés et aux méthodes de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cd8ef-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cd8ef-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="cd8ef-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="cd8ef-110">Affichage du nom de l'application, de la version et de l'identificateur de langue</span><span class="sxs-lookup"><span data-stu-id="cd8ef-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="cd8ef-p103">Dans l'exemple suivant, les propriétés [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) et [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) permettent de renvoyer le nom et le numéro de version de l'instance InfoPath. La propriété [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) est ensuite utilisée pour renvoyer un objet **LanguageSettings** qui à son tour permet de renvoyer le code LCID (nombre de quatre chiffres) de la langue actuellement utilisée pour l'interface utilisateur InfoPath. Enfin, toutes ces informations sont affichées dans une zone de message.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-p103">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath. The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language. Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cd8ef-p104">[!IMPORTANTE] Pour que la propriété **LanguageSettings** fonctionne, vous devez établir une référence à la bibliothèque d'objets Microsoft Office 14.0 (sous l'onglet **COM** de la boîte de dialogue **Ajouter une référence** dans Visual Studio 2012). Cette opération établit une référence à l'espace de noms **Microsoft.Office.Core**, qui contient la classe **LanguageSettings**. En outre, le formulaire doit être exécuté au niveau Confiance totale.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-p104">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012. This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class. Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="cd8ef-117">Cet exemple a besoin d'une directive **using** ou **Imports** pour l'espace de noms **Microsoft.Office.Core** dans la section des déclarations du module de code du formulaire.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
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


