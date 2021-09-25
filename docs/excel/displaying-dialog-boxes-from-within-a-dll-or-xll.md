---
title: Affichage des boîtes de dialogue à partir d’une DLL ou d’une XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], displaying dialog boxes from,dialog boxes [Excel 2007], displaying from a DLL or XLL,DLLs [Excel 2007], displaying dialog boxes from
ms.localizationpriority: medium
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a01cd39c81d88655f7e8c3c865292d657eee2c57
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576701"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Affichage des boîtes de dialogue à partir d’une DLL ou d’une XLL

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour afficher une boîte de dialogue Win32 à l’aide, par exemple, de la fonction SDK Windows **DialogBox**, vous devez d’abord obtenir l’instance 32 bits complète et les poignées de fenêtre principale pour Excel. Pour plus d’informations, [voir Access Excel Instance et Handles de fenêtre principale.](how-to-access-excel-instance-and-main-window-handles.md) 
  
En supposant que votre projet contient la ressource de boîte de dialogue, vous devez suivre plusieurs étapes pour définir la routine de gestion des messages sur celle de la boîte de dialogue qui vient d’être affichée et pour restaurer la routine de gestion des messages Excel lorsque la boîte de dialogue est fermée. L’exemple [de commande fShowDialog](fshowdialog.md) dans le projet Generic illustre l’utilisation des fonctions Windows pour le faire correctement. 
  
Vous pouvez également afficher des boîtes de dialogue à l’aide de l’API C sans avoir à utiliser Windows fonctions du SDK. Toutefois, les fonctionnalités de la boîte de dialogue de l’API C sont très limitées par rapport à celles de Windows, Visual Basic pour Applications (VBA) ou microsoft Foundation Classes (MFC). (Par exemple, les boîtes de dialogue api C sont toujours modales).
  
## <a name="see-also"></a>Voir aussi



[Création de XLL](creating-xlls.md)
  
[Développement des fichiers DLL](developing-dlls.md)
  
[Accès à l’instance Excel et aux handles de fenêtre principaux](how-to-access-excel-instance-and-main-window-handles.md)
  
[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

