---
title: HelpContext, HelpFile, propriétés (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291991"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext, HelpFile, propriétés (ADO)

**S’applique à** : Access 2013, Office 2013

Indique le fichier d'aide et la rubrique associés à un objet [Error](error-object-ado.md).

## <a name="return-values"></a>Valeurs de retour

- **HelpContextID**: renvoie un ID de contexte pour une rubrique de fichier d'aide sous forme de valeur **Long**.

- **HelpFile** : renvoie une valeur **String** qui correspond à un chemin d'accès à un fichier d'aide entièrement résolu.

## <a name="remarks"></a>Remarques

Si un fichier d'aide est spécifié dans la propriété **HelpFile**, la propriété **HelpContext** permet d'afficher automatiquement la rubrique d'aide qu'elle identifie. Si aucune rubrique d'aide pertinente n'est disponible, la propriété **HelpContext** renvoie zéro et la propriété **HelpFile** renvoie une chaîne vide («   »).

