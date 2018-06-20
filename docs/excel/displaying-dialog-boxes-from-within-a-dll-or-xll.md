---
title: Affichage des boîtes de dialogue à partir d’une DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [excel 2007], affichage des boîtes de dialogue, boîtes de dialogue [Excel 2007], affichage à partir d’une DLL ou XLL, affichage des boîtes de dialogue à partir de DLL [Excel 2007],
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782028"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Affichage des boîtes de dialogue à partir d’une DLL ou XLL

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour afficher une boîte de dialogue Win32 à l’aide, par exemple, la fonction Windows SDK **DialogBox**, vous devez d’abord obtenir l’instance 32 bits complète et les poignées de la fenêtre principale pour Excel. Pour plus d’informations, voir [accès Instance d’Excel et gère les fenêtre principale](how-to-access-excel-instance-and-main-window-handles.md). 
  
En supposant que votre projet contienne la ressource de boîte de dialogue, vous devez effectuer plusieurs étapes de la routine de gestion des messages à celle de la boîte de dialogue affiché et pour restaurer le message Excel routine de gestion des lors de la fermeture de la boîte de dialogue. La commande d’exemple [fShowDialog](fshowdialog.md) dans le projet générique illustre l’utilisation des fonctions Windows pour ce faire correctement. 
  
Vous pouvez également afficher les boîtes de dialogue sans avoir à utiliser les fonctions du Kit de développement Windows à l’aide de l’API C. Toutefois, les fonctionnalités de boîte de dialogue de l’API C sont limitées par rapport à ceux de Windows, Visual Basic pour Applications (VBA) ou les Classes MFC (Microsoft Foundation). (Par exemple, les boîtes de dialogue API C sont toujours modales).
  
## <a name="see-also"></a>Voir aussi



[Cr�ation de XLL](creating-xlls.md)
  
[D�veloppement de DLL](developing-dlls.md)
  
[Instance d’Excel Access et les poignées de la fenêtre principale](how-to-access-excel-instance-and-main-window-handles.md)
  
[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

