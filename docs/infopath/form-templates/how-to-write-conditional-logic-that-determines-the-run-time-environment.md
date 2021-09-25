---
title: Écrire une logique conditionnelle qui détermine l’environnement d’exécuter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- running in infopath [infopath 2007],run-time environment [InfoPath 2007],running in browser [InfoPath 2007],InfoPath 2007, determining run-time environment
ms.localizationpriority: medium
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: La propriété Environment de la classe Application obtient une référence à un objet Environment qui peut être utilisé pour déterminer l'environnement d'exécution (InfoPath, navigateur Web ou navigateur mobile) utilisé pour ouvrir le formulaire.
ms.openlocfilehash: 347633f0dc13b8b001ca146cd56aa734c0edc8b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625818"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Écrire une logique conditionnelle qui détermine l’environnement d’exécuter

La propriété [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtient une référence à un objet [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) qui peut être utilisé pour déterminer l'environnement d'exécution (InfoPath, navigateur Web ou navigateur mobile) utilisé pour ouvrir le formulaire. 
  
## <a name="example"></a>Exemple

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Détermination de l'environnement d'exécution d'un formulaire

La classe [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) fournit les propriétés [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) et [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) qui permettent de déterminer l'environnement d'édition utilisé pour ouvrir un modèle de formulaire. Si les deux propriétés renvoient **false**, le modèle de formulaire a été ouvert dans l'éditeur Microsoft InfoPath. Si l'une ou l'autre des propriétés renvoie **true**, le modèle de formulaire a été ouvert à partir d'une bibliothèque de documents configurée de manière appropriée dans Microsoft SharePoint Server 2010 qui exécute InfoPath Forms Services dans le programme pour la propriété correspondante : un navigateur Web (propriété [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ) ou un navigateur mobile (propriété [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ). 
  
Dans l'exemple suivant, si le formulaire est ouvert dans un navigateur ou un navigateur mobile, la valeur de champ1 (qui est liée à un contrôle **Zone de texte**) est définie sur une chaîne pour indiquer l'environnement d'exécution dans lequel le formulaire a été ouvert. S'il est ouvert dans InfoPath, la méthode **System.Windows.Forms.MessageBox.Show** (qui n'est pas disponible lorsqu'un formulaire est exécuté dans un navigateur) est utilisée pour afficher une zone de message. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Lorsque vous créez le modèle de formulaire pour l'exemple de code ci-dessous, sélectionnez le modèle **Vide** sous l'onglet **Nouveau** de la vue Backstage (vous pouvez également sélectionner **Formulaire de navigateur Web** dans la liste déroulante **Type de formulaire** dans la catégorie **Compatibilité** de la boîte de dialogue **Options de formulaire**). Pour prendre en charge la classe **MessageBox**, ajoutez une référence à **System.Windows.Forms** sous l'onglet . **NET** de la boîte de dialogue **Ajouter une référence** dans Visual Studio 2012, puis ajoutez une directive **using** ou **Imports** pour **System.Windows.Forms** dans la section des déclarations du module de code du formulaire. 
  
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


