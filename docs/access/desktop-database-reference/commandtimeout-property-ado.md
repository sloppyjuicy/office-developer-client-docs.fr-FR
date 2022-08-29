---
title: CommandTimeout, propriété (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6f590155a043b3dea42f20cf1922bcbcf8f68c9a
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365970"
---
# <a name="commandtimeout-property-ado"></a>CommandTimeout, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le délai d'attente pour l'exécution d'une commande avant l'abandon de la tentative et la génération d'une erreur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** indiquant, en secondes, le délai d'attente pour l'exécution d'une commande. La valeur par défaut est 30.

## <a name="remarks"></a>Remarques

Utilisez la propriété **CommandTimeout** dans un objet [Connection](connection-object-ado.md) ou [Command](command-object-ado.md) pour permettre l'annulation d'un appel de la méthode [Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-command), en raison d'un délai dû au trafic réseau ou à une utilisation intensive du serveur. Si l'intervalle défini dans la propriété **CommandTimeout** s'écoule avant que la commande ait fini de s'exécuter, une erreur se produit et ADO annule la commande. Si vous attribuez la valeur 0 à la propriété, ADO attend indéfiniment que l'exécution se termine. Assurez-vous que le fournisseur et la source de données dans lesquels vous écrivez le code prennent en charge la fonctionnalité **CommandTimeout**.

Le paramètre de **CommandTimeout** d'un objet **Connection** n'a aucun effet sur le paramètre de **CommandTimeout** d'un objet **Command** sur le même objet **Connection**. En d'autres termes, la propriété **CommandTimeout** de l'objet **Command** n'hérite pas de la valeur de la propriété **CommandTimeout** de l'objet **Connection**.

On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.

