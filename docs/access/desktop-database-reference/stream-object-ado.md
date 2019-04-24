---
title: Stream, objet (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f6d7e8f64f6b14ea699006fc0461cdf0ded2a06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308483"
---
# <a name="stream-object-ado"></a>Stream, objet (ADO)


**S’applique à** : Access 2013, Office 2013

Représente un flux de données binaires ou de texte.

## <a name="remarks"></a>Remarques

Dans les hiérarchies structurées en arborescence telles qu'un système de fichiers ou un système de messagerie, un flux binaire par défaut de bits peut être associé à un [enregistrement](record-object-ado.md) qui contient le contenu du fichier ou du courrier électronique. Un objet **Stream** peut être utilisé pour manipuler des champs ou des enregistrements contenant ces flux de données. Un objet **Stream** peut être obtenu de différentes façons :

  - À partir d'une URL pointant sur un objet (en général, un fichier) contenant des données binaires ou texte. Cet objet peut être un simple document, un objet **Record** représentant un document structuré ou un dossier.

  - En ouvrant l'objet **Stream** par défaut associé à un objet **Record**. Vous pouvez obtenir le flux par défaut associé à un objet **Record** lorsque cet objet **Record** est ouvert, ce qui évite un aller-retour qui ne servirait qu'à ouvrir le flux.

  - Par l'instanciation d'un objet **Stream**. Ces objets **Stream** peuvent être utilisés pour stocker des données afin de répondre aux besoins de votre application. Contrairement au **Stream** associé à une URL ou au **Stream** par défaut d'un **Record**, un **Stream** instancié n'est pas associé à une source sous-jacente par défaut.

Les méthodes et les propriétés d'un objet **Stream** vous permettent d'effectuer diverses tâches :

  - ouvrir un objet **Stream** à partir d'un **Record** ou d'une URL, à l'aide de la méthode [Open](open-method-ado-stream.md) ;

  - fermer un **Stream** à l'aide de la méthode [Close](close-method-ado.md) ;

  - entrer des octets ou du texte dans un **Stream** à l'aide des méthodes [Write](write-method-ado.md) et [WriteText](writetext-method-ado.md) ;

  - lire des octets du **Stream** à l'aide des méthodes [Read](read-method-ado.md) et [ReadText](readtext-method-ado.md) ;

  - écrire des données **Stream** (encore présentes dans le tampon ADO) dans l'objet sous-jacent à l'aide de la méthode [Flush](flush-method-ado.md) ;

  - copier le contenu d'un **Stream** dans un autre **Stream** à l'aide de la méthode [CopyTo](copyto-method-ado.md) ;

  - contrôler la façon dont les lignes sont lues depuis le fichier source avec la méthode [SkipLine](skipline-method-ado.md) et la propriété [LineSeparator](lineseparator-property-ado.md) ;

  - déterminer la fin de la position du flux à l'aide de la propriété [EOS](eos-property-ado.md) et de la méthode [SetEOS](seteos-method-ado.md) ;

  - enregistrer et restaurer des données dans des fichiers à l'aide des méthodes [SaveToFile](savetofile-method-ado.md) et [LoadFromFile](loadfromfile-method-ado.md) ;

  - spécifier le jeu de caractères utilisé pour stocker le **Stream** à l'aide de la propriété [Charset](charset-property-ado.md) ;

  - arrêter une opération **Stream** asynchrone à l'aide de la méthode [Cancel](cancel-method-ado.md) ;

  - déterminer le nombre d'octets d'un **Stream** à l'aide de la propriété [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) ;

  - contrôler la position actuelle au sein d'un **Stream** à l'aide de la propriété [Position](position-property-ado.md) ;

  - déterminer le type de données dans un **Stream** à l'aide de la propriété [Type](type-property-ado-stream.md) ;

  - déterminer l'état actuel du **Stream** (fermé, ouvert ou en cours d'exécution) à l'aide de la propriété [State](state-property-ado.md) ;

  - spécifier le mode d'accès au **Stream** à l'aide de la propriété [Mode](mode-property-ado.md).

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le modèle http appellent automatiquement [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d'informations, consultez la rubrique [URL absolues et relatives](absolute-and-relative-urls.md).


