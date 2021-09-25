---
title: Convertir des tableaux, des formulaires et des rapports Microsoft Access
TOCTitle: Convert Microsoft Access tables, forms, and reports
description: Les modifications introduites par Microsoft Access 2002 peuvent affecter le comportement de vos applications de version 1.x ou 2.0.
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7a3eec5e642f4a307fc9f0e812206d1360560f4a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569278"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Convertir des tableaux, des formulaires et des rapports Microsoft Access

**S’applique à** : Access 2013, Office 2013

Plusieurs modifications introduites par Microsoft Access 2002 risquent d'affecter le fonctionnement de vos applications des versions 1.*x* et 2.0. Les sections suivantes vous apportent plus d'informations sur ces modifications.

## <a name="indexes-and-relationships"></a>Index et relations

Une table Microsoft Access peut contenir jusqu'à 32 index. Des tables très complexes faisant partie de plusieurs relations peuvent parfois dépasser le nombre d'index permis ; vous ne pourrez dès lors pas convertir la base de données qui contient ces tables. Le moteur de base de données Microsoft Access crée des index des deux côtés des relations entre les tables. Si vous ne parvenez pas à convertir votre base de données, supprimez quelques relations et essayez de nouveau.

## <a name="the-limittolist-property-of-combo-boxes"></a>Propriété LimitToList des zones de liste déroulante

Dans Microsoft Access 2002 ou une édition ultérieure, les zones de liste déroulante acceptent des valeurs **Null** lorsque la propriété **LimitToList** est définie sur **True** (–1), que la liste contienne ou non des valeurs **Null.** In version 2.0, a combo box that has the **LimitToList** property set to **True** won't accept a **Null** value unless the list contains a **Null** value. If you want to prevent users from entering a **Null** value by using a combo box, set the **Required** property of the field in the table to **Yes**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Menus et activation sur place des objets OLE

Pour mettre à votre disposition des fonctionnalités supplémentaires lors de l’activation des objets OLE sur place, certaines commandes de menu peuvent avoir été déplacées vers un menu qui n’est pas remplacé lorsque vous activez un serveur OLE.

Les macros de votre application convertie qui utilisent une action ExécuterElémentMenu pour exécuter une commande de menu de la version 2.0 lors de l'activation d'une application ne seront pas affectées par les modifications. Les commandes de la version 2.0 correspondent à leur équivalent dans les versions ultérieures de Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Référencement d’un contrôle sur un formulaire en lecture seule

Dans Microsoft Access 2002 ou une version ultérieure, vous ne pouvez pas utiliser d'expression pour faire référence à la valeur d'un contrôle de formulaire en lecture seule qui lié d'une source d'enregistrement vide. Dans les versions précédentes, l'expression renvoyait la valeur **Null**. Avant de faire référence à un contrôle dans un formulaire en lecture seule, vous devez vérifier que la source d'enregistrement du formulaire contient des enregistrements.

## <a name="date-fields-and-data-entry"></a>Champs de date et entrée de données

Si vous tapez **3/3** dans un champ de type Date d'une feuille de données de formulaire ou de table, Microsoft Access 2002, ou une version ultérieure, y insère automatiquement l'année en cours. Toutefois, si vous tapez **3/3/** dans le même champ, Microsoft Access renvoie un message d'erreur. Vous devez omettre le dernier délimiteur de date, afin que Microsoft Access puisse convertir la date dans le format correct.

## <a name="buttons-created-with-the-command-button-wizard"></a>Boutons créés avec l’Assistant Bouton de commande

Si vous utilisiez l'Assistant Bouton de commande dans les versions 2.0 et 7.0 de Microsoft Access pour générer du code qui appelait une autre application, vous devez supprimer le bouton et le créer de nouveau à l'aide de l'Assistant Bouton de commande de Microsoft Access 2002 ou version ultérieure.

## <a name="form-and-report-class-modules"></a>Modules de classe de formulaire et d’état

In versions of Microsoft Access prior to 2002, **Form** and **Report** objects have associated class modules even if there's no code behind the object. In Microsoft Access 2002 or later, you can set a form's or report's **HasModule** property to **False**. When you set the **HasModule** property to **False**, the form or report will take up less disk space and will load faster because it will no longer have an associated class module.

## <a name="converted-version-20-report-has-different-margins"></a>Le rapport converti version 2.0 présente des marges différentes

Vous rencontrerez peut-être des problèmes lors de l'impression ou de l'affichage en mode Aperçu avant impression d'un état dans Microsoft Access 2002 ou version ultérieure qui a été converti à partir de Microsoft Access 2.0 si certaines de ses marges ont pour valeur 0. Lorsque vous convertissez un état Microsoft Access 2.0, les marges n'ont pas pour valeur 0 ; elles se voient attribuer la valeur minimale de marge valide pour l'imprimante par défaut. Cela empêche ainsi l'état d'imprimer des données dans la zone non imprimable de l'imprimante.

Pour résoudre ce problème, réduisez la largeur des colonnes, l'espace entre les colonnes et le nombre de colonnes dans l'état, de sorte que la largeur des colonnes ajoutée à la largeur des marges par défaut soit égale ou inférieure à la largeur de votre papier.

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Can’t use the Format property to distinguish Null values and zero-length strings

Dans les versions 1. *x* et 2.0, vous pouvez utiliser la propriété **Format** d’un contrôle pour afficher différentes valeurs pour les valeurs **Null** et les chaînes de longueur nulle ( » « ). Dans Microsoft Access 2002 ou version ultérieure, pour distinguer les valeurs de type **Null** des chaînes vides dans un contrôle de formulaire, paramétrez la propriété **ControlSource** d'un contrôle sur une expression qui teste la présence de valeurs **Null**. Par exemple, pour afficher « Null » ou « ZLS » dans un contrôle, paramétrez sa propriété **ControlSource** sur l'expression suivante :

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`

