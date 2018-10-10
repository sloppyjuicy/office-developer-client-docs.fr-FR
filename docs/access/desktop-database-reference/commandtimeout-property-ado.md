---
title: CommandTimeout, propriété (ADO)
TOCTitle: CommandTimeout Property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 58d95f6a3238d09ae10ddb3ba127a9fa68631f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469878"
---
# <a name="commandtimeout-property-ado"></a>CommandTimeout, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le délai d'attente pour l'exécution d'une commande avant l'abandon de la tentative et la génération d'une erreur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** indiquant, en secondes, le délai d'attente pour l'exécution d'une commande. La valeur par défaut est 30.

## <a name="remarks"></a>Notes

Utilisez la propriété **CommandTimeout** dans un objet [Connection](connection-object-ado.md) ou [Command](command-object-ado.md) pour permettre l'annulation d'un appel de la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), en raison d'un délai dû au trafic réseau ou à une utilisation intensive du serveur. Si l'intervalle défini dans la propriété **CommandTimeout** s'écoule avant que la commande ait fini de s'exécuter, une erreur se produit et ADO annule la commande. Si vous attribuez la valeur 0 à la propriété, ADO attend indéfiniment que l'exécution se termine. Assurez-vous que le fournisseur et la source de données dans lesquels vous écrivez le code prennent en charge la fonctionnalité **CommandTimeout**.

Le paramètre de **CommandTimeout** d'un objet **Connection** n'a aucun effet sur le paramètre de **CommandTimeout** d'un objet **Command** sur le même objet **Connection**. En d'autres termes, la propriété **CommandTimeout** de l'objet **Command** n'hérite pas de la valeur de la propriété **CommandTimeout** de l'objet **Connection**.

Sur un objet **Connection** , la propriété **CommandTimeout** reste en lecture/écriture après l’ouverture de la **connexion** .

