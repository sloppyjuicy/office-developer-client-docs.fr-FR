---
title: Flush, méthode - ActiveX Data Objects (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ecf56ccf715df324798cd9b5adfc57f92591f05
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885128"
---
# <a name="flush-method-ado"></a>Flush, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Force l'envoi de l'objet [Stream](stream-object-ado.md) conservé dans la mémoire tampon ADO vers l'objet sous-jacent auquel cet objet **Stream** est associé.

## <a name="syntax"></a>Syntaxe

*Flux de données*. Vider

## <a name="remarks"></a>Notes

Cette méthode peut servir à envoyer le contenu de la mémoire tampon du flux vers l'objet sous-jacent (par exemple, le nœud ou le fichier représenté par l'URL qui est la source de l'objet **Stream** ). Cette méthode doit être appelée lorsque vous souhaitez vous assurer que toutes les modifications apportées à un objet **Stream** ont été écrites. Toutefois, il n'est généralement pas nécessaire d'appeler la méthode **Flush** avec ADO, dans la mesure où ADO vide continuellement sa mémoire tampon en arrière-plan dans la mesure du possible. Les modifications apportées à un objet **Stream** sont effectuées automatiquement et ne sont pas mises en cache jusqu'à l'appel de la méthode **Flush**.

La fermeture d'un objet **Stream** avec la méthode [Close](close-method-ado.md) vide automatiquement le contenu d'un objet **Stream**; il n'est pas nécessaire d'appeler explicitement la méthode **Flush** immédiatement avant l'appel de la méthode **Close**.

