---
title: Écrire une logique conditionnelle qui détermine l’environnement d’exécuter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- running in infopath [infopath 2007],run-time environment [InfoPath 2007],running in browser [InfoPath 2007],InfoPath 2007, determining run-time environment
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: La propriété Environment de la classe Application obtient une référence à un objet Environment qui peut être utilisé pour déterminer l'environnement d'exécution (InfoPath, navigateur Web ou navigateur mobile) utilisé pour ouvrir le formulaire.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408599"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="651c7-104">Écrire une logique conditionnelle qui détermine l’environnement d’exécuter</span><span class="sxs-lookup"><span data-stu-id="651c7-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="651c7-105">La propriété [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtient une référence à un objet [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) qui peut être utilisé pour déterminer l'environnement d'exécution (InfoPath, navigateur Web ou navigateur mobile) utilisé pour ouvrir le formulaire.</span><span class="sxs-lookup"><span data-stu-id="651c7-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="651c7-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="651c7-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="651c7-107">Détermination de l'environnement d'exécution d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="651c7-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="651c7-p101">La classe [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) fournit les propriétés [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) et [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) qui permettent de déterminer l'environnement d'édition utilisé pour ouvrir un modèle de formulaire. Si les deux propriétés renvoient **false**, le modèle de formulaire a été ouvert dans l'éditeur Microsoft InfoPath. Si l'une ou l'autre des propriétés renvoie **true**, le modèle de formulaire a été ouvert à partir d'une bibliothèque de documents configurée de manière appropriée dans Microsoft SharePoint Server 2010 qui exécute InfoPath Forms Services dans le programme pour la propriété correspondante : un navigateur Web (propriété [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ) ou un navigateur mobile (propriété [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="651c7-p101">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template. If both properties return **false**, the form template was opened in the Microsoft InfoPath editor. If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="651c7-p102">Dans l'exemple suivant, si le formulaire est ouvert dans un navigateur ou un navigateur mobile, la valeur de champ1 (qui est liée à un contrôle **Zone de texte**) est définie sur une chaîne pour indiquer l'environnement d'exécution dans lequel le formulaire a été ouvert. S'il est ouvert dans InfoPath, la méthode **System.Windows.Forms.MessageBox.Show** (qui n'est pas disponible lorsqu'un formulaire est exécuté dans un navigateur) est utilisée pour afficher une zone de message.</span><span class="sxs-lookup"><span data-stu-id="651c7-p102">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in. If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="651c7-p103">[!IMPORTANTE] Lorsque vous créez le modèle de formulaire pour l'exemple de code ci-dessous, sélectionnez le modèle **Vide** sous l'onglet **Nouveau** de la vue Backstage (vous pouvez également sélectionner **Formulaire de navigateur Web** dans la liste déroulante **Type de formulaire** dans la catégorie **Compatibilité** de la boîte de dialogue **Options de formulaire**). Pour prendre en charge la classe **MessageBox**, ajoutez une référence à **System.Windows.Forms** sous l'onglet . **NET** de la boîte de dialogue **Ajouter une référence** dans Visual Studio 2012, puis ajoutez une directive **using** ou **Imports** pour **System.Windows.Forms** dans la section des déclarations du module de code du formulaire.</span><span class="sxs-lookup"><span data-stu-id="651c7-p103">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view. (Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the . **NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


