---
title: Affichage des boîtes de dialogue dans un fichier DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [Excel 2007], affichage des boîtes de dialogue à partir de, boîtes de dialogue [Excel 2007], affichage à partir d'un fichier DLL ou XLL, dll [Excel 2007], affichage des boîtes de dialogue à partir de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310934"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Affichage des boîtes de dialogue dans un fichier DLL ou XLL

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour afficher une boîte de dialogue Win32 en utilisant, par exemple, la fonction **DialogBox**du kit de développement logiciel (SDK) Windows, vous devez d'abord obtenir l'instance complète de 32 bits et les principaux handles de fenêtre pour Excel. Pour plus d'informations, consultez la rubrique [Access Excel instance and principal Window Handles](how-to-access-excel-instance-and-main-window-handles.md). 
  
En supposant que votre projet contient la ressource de la boîte de dialogue, vous devez effectuer plusieurs étapes pour définir la routine de gestion des messages sur celle de la boîte de dialogue nouvellement affichée et pour restaurer la routine de gestion des messages Excel lors de la fermeture de la boîte de dialogue. L'exemple de commande [fShowDialog](fshowdialog.md) dans le projet générique illustre l'utilisation des fonctions Windows pour effectuer correctement cette opération. 
  
Vous pouvez également afficher des boîtes de dialogue à l'aide de l'API C sans avoir à utiliser les fonctions du kit de développement logiciel Windows. Toutefois, les fonctionnalités de boîte de dialogue de l'API C sont très limitées par rapport à celles de Windows, de Visual Basic pour applications (VBA) ou de Microsoft Foundation classes (MFC). (Par exemple, les boîtes de dialogue de l'API C sont toujours modales).
  
## <a name="see-also"></a>Voir aussi



[Création de XLL](creating-xlls.md)
  
[D�veloppement de DLL](developing-dlls.md)
  
[Accès à l’instance Excel et aux handles de fenêtre principaux](how-to-access-excel-instance-and-main-window-handles.md)
  
[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

