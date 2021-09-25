---
title: Traitement des transactions
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1b8c41443a5fc17101edd262b7bac04cb076666b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562159"
---
# <a name="transaction-processing"></a>Traitement de transactions

**S’applique à** : Access 2013, Office 2013

ADO fournit les méthodes suivantes pour le contrôle des transactions : **BeginTrans**, **CommitTrans** et **RollbackTrans**. Utilisez ces méthodes avec un objet **Connection** pour enregistrer ou annuler en bloc une série de modifications apportées à la source de données. Par exemple, pour un transfert financier entre deux comptes, vous devez soustraire un montant de l'un et ajouter ce même montant à l'autre. Si l'une des deux mises à jour échoue, les comptes ne sont pas équilibrés. Si ces modifications sont effectuées par l'intermédiaire d'une transaction ouverte, vous êtes assuré de l'échec ou de la réussite de toutes les modifications.

> [!NOTE]
> Tous les fournisseurs ne prennent pas en charge les transactions. Vérifiez que la propriété « **Transaction DDL** », définie par le fournisseur, apparaît dans la collection [Properties](properties-collection-ado.md) de l’objet **Connection** ; elle indique que le fournisseur prend en charge les transactions. Si ce n’est pas le cas, l’appel de l’une de ces méthodes retourne une erreur.

Après l'appel de la méthode **BeginTrans**, le fournisseur ne validera plus les modifications instantanément. Vous devrez, pour cela, appeler les méthodes **CommitTrans** ou **RollbackTrans** pour clôturer la transaction.

L'appel de la méthode **CommitTrans** permet d'enregistrer les modifications apportées à une transaction ouverte sur la connexion et de clôturer la transaction. L'appel de la méthode **RollbackTrans** permet d'annuler toutes les modifications effectuées dans une transaction ouverte et de clôturer la transaction. L'appel de l'une ou l'autre méthode sans transaction ouverte provoque une erreur.

En fonction de la propriété **Attributes** de l'objet [Connection](attributes-property-ado.md), l'appel des méthodes **CommitTrans** ou **RollbackTrans** permet de lancer automatiquement une nouvelle transaction. Si la propriété **Attributes** a la valeur **adXactCommitRetaining**, le fournisseur lance automatiquement une nouvelle transaction après un appel à **CommitTrans**. Si la propriété **Attributes** a la valeur **adXactAbortRetaining**, le fournisseur lance automatiquement une nouvelle transaction après un appel à **RollbackTrans**.

## <a name="transaction-isolation-level"></a>Niveau d’isolation des transactions

La propriété **IsolationLevel** permet de définir le niveau d'isolation d'une transaction sur un objet **Connection**. Le paramètre ne prend effet qu'au prochain appel de la méthode [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si le niveau d'isolation demandé n'est pas disponible, le fournisseur peut renvoyer le niveau d'isolation le plus élevé suivant. Reportez-vous **à la propriété IsolationLevel** dans la référence du programmeur ADO pour plus d’informations sur les valeurs valides.

## <a name="nested-transactions"></a>Transactions imbrmbrées

Pour les fournisseurs qui prennent en charge les transactions imbriquées, l'appel de la méthode **BeginTrans** dans une transaction ouverte permet de lancer une nouvelle transaction imbriquée. La valeur de retour indique le niveau d'imbrication : une valeur de retour « 1 » indique que vous avez ouvert une transaction de niveau supérieur (la transaction n'est pas imbriquée dans une autre transaction) « 2 » indique que vous avez ouvert une transaction de second niveau (une transaction imbriquée dans une transaction de niveau supérieur) etc... L'appel de **CommitTrans** ou de **RollbackTrans** n'affecte que la dernière transaction ouverte. Vous devez fermer ou annuler la transaction active avant de pouvoir résoudre une transaction de niveau supérieur.

