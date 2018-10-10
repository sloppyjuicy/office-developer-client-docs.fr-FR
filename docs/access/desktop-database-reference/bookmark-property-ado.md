---
title: Bookmark, propriété (ADO)
TOCTitle: Bookmark Property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a89be0ad75ea84faa9fe17834260832070dd7578
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470758"
---
# <a name="bookmark-property-ado"></a>Bookmark, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique un signet qui identifie de manière unique l'enregistrement actif d'un objet [Recordset](recordset-object-ado.md) ou définit comme enregistrement actif d'un objet **Recordset** l'enregistrement identifié par un signet valide.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une expression de type **Variant** qui correspond à un signet valide.

## <a name="remarks"></a>Notes

Utilisez la propriété **Bookmark** pour enregistrer la position de l'enregistrement actif et revenir à cet enregistrement à tout moment. Les signets ne sont disponibles que dans les objets **Recordset** prenant en charge la fonctionnalité de signet.

Lorsque vous ouvrez un objet **Recordset**, chacun de ses enregistrements possède un signet unique. Pour enregistrer le signet de l'enregistrement actif, affectez une variable comme valeur de la propriété **Bookmark**. Pour revenir rapidement à cet enregistrement à tout moment après avoir accédé à un autre enregistrement, affectez à la propriété **Bookmark** de l'objet **Recordset** la valeur de cette variable.

L'utilisateur n'est peut-être pas en mesure de visualiser la valeur du signet. De même, les utilisateurs ne doivent pas s'attendre à pouvoir comparer directement des signets : deux signets renvoyant au même enregistrement peuvent avoir des valeurs différentes.

Si vous utilisez la méthode [Clone](clone-method-ado.md) pour créer une copie d'un objet **Recordset**, les paramètres de la propriété **Bookmark** des objets **Recordset** d'origine et dupliqué, sont identiques et vous pouvez les utiliser de manière interchangeable. Cependant, vous ne pouvez pas utiliser des signets de différents objets **Recordset** de manière interchangeable même s'ils ont été créés à partir de la même source ou de la même commande.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet **Recordset** de côté client, la propriété **Bookmark** est toujours disponible.

