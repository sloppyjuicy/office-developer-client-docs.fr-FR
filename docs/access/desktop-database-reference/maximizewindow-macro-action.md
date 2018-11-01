---
title: AgrandirFenêtre, action de macro
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 110262c9aee48fc24858150714194953136fa835
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867271"
---
# <a name="maximizewindow-macro-action"></a>AgrandirFenêtre, action de macro


**S’applique à**: Access 2013, Office 2013

Si Access est configuré pour utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l’action **Agrandirfenêtre** pour agrandir la fenêtre active afin qu’elle remplisse la fenêtre Access. Cette action vous permet de voir la plus grande partie possible de l'objet dans la fenêtre active.


> [!NOTE]
> <P>[!REMARQUE] Cette action ne peut être appliquée aux fenêtres de code dans Visual Basic Editor. Pour plus d'informations sur la façon d'affecter des fenêtres de code, reportez-vous à la rubrique relative à la propriété <STRONG>WindowState</STRONG>.</P>



## <a name="setting"></a>Valeur

L'action **AgrandirFenêtre** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Cette action équivaut à cliquer sur le bouton **Agrandir** dans le coin supérieur droit de la fenêtre ou à cliquer sur **Agrandir** dans le menu **Contrôle** de la fenêtre.

Vous pouvez utiliser l'action **RestaurerFenêtre** pour rétablir la taille initiale de la fenêtre agrandie.

**Conseils**

  - Vous devrez peut-être utiliser la méthode **SélectionnerObjet** si la fenêtre que vous voulez agrandir n'est pas la fenêtre active.

  - Si vous agrandissez une fenêtre dans Microsoft Access, toutes les autres fenêtres sont également agrandies lors de leur ouverture ou de leur activation. Cependant, la taille des formulaires indépendants reste inchangée. Pour qu'un formulaire conserve sa taille d'origine lorsque vous agrandissez d'autres fenêtres, attribuez la valeur **Oui** à sa propriété **FenIndépendante**.

Pour exécuter l'action **AgrandirFenêtre** dans un module Visual Basic pour Applications, utilisez la méthode **Maximize** de l'objet **DoCmd**.

