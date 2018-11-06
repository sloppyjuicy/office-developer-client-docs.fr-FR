---
title: Fonctionnement conjoint des gestionnaires d’événements
TOCTitle: How event handlers work together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a397b0f88bb60552a6e53432a3c8c4d788013103
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997271"
---
# <a name="how-event-handlers-work-together"></a>Fonctionnement conjoint des gestionnaires d’événements

**S’applique à**: Access 2013, Office 2013

À moins que vous ne programmiez en Visual Basic, tous les gestionnaires des événements **Connection** et **Recordset** doivent être implémentés, que vous décidiez de traiter ou non tous les événements. La charge de travail qu'implique cette implémentation dépend de votre langage de programmation. Pour plus d'informations, consultez [Instanciation des événements ADO par langage](https://msdn.microsoft.com/library/jj250244\(v=office.15\)).

## <a name="paired-event-handlers"></a>Gestionnaires d’événements associés

Chaque gestionnaire d'événements Will est associé à un gestionnaire d'événements Complete. Par exemple, lorsque votre application modifie la valeur d'un champ, le gestionnaire d'événements **WillChangeField** est appelé. Si la modification est acceptable, l'application conserve le paramètre **adStatus** inchangé et l'opération est effectuée. Au terme de l'opération, un événement **FieldChangeComplete** notifie votre application que l'opération est terminée. Si elle s'est correctement déroulée, le paramètre **adStatus** contient **adStatusOK**. Dans le cas contraire, **adStatus** contient **adStatusErrorsOccurred**. Vous devez alors examiner l'objet **Error** pour déterminer la cause de l'erreur.

Lorsque **WillChangeField** est appelé, vous pouvez décider de ne pas apporter de modification. Dans ce cas, **adStatus** doit être défini avec la valeur **adStatusCancel**. L'opération est annulée et l'événement **FieldChangeComplete** reçoit un paramètre **adStatus** avec la valeur **adStatusErrorsOccurred**. L'objet **Error** contient **adErrOperationCancelled** de sorte que le gestionnaire **FieldChangeComplete** sait que l'opération a été annulée. Toutefois, vous devez vérifier la valeur du paramètre **adStatus** avant de le modifier, car la définition de **adStatus** à **adStatusCancel** n'a aucune incidence si le paramètre avait la valeur **adStatusCantDeny** au moment où vous avez commencé la procédure.

Il arrive qu'une opération génère plusieurs événements. Par exemple, l'objet **Recordset** possède des événements associés lorsque des objets **Field** et **Record** sont modifiés. Lorsque votre application modifie la valeur d'un objet **Field**, le gestionnaire d'événements **WillChangeField** est appelé. S'il détermine que l'opération peut continuer, le gestionnaire d'événements **WillChangeRecord** est également appelé. Si celui-ci autorise également l'événement à se poursuivre, la modification a lieu et les gestionnaires d'événements **FieldChangeComplete** et **RecordChangeComplete** sont appelés. L'ordre dans lequel les gestionnaires d'événements Will pour une opération donnée sont appelés n'est pas défini. Pour cette raison, évitez d'écrire du code reposant sur un ordre précis des appels des gestionnaires.

Dans les cas où plusieurs événements Will sont générés, il se peut que l'un d'entre eux annule l'opération en attente. Par exemple, si votre application modifie la valeur d'un objet **Field**, les gestionnaires d'événements **WillChangeField** et **WillChangeRecord** doivent normalement être appelés tous les deux. Cependant, si l'opération est annulée dans le premier gestionnaire d'événements, le gestionnaire Complete associé est immédiatement appelé avec **adStatusOperationCancelled**. Le second gestionnaire d'événements n'est jamais appelé. Si, toutefois, le premier gestionnaire événements autorise l'événement à se poursuivre, le second est appelé. S'il annule ensuite l'opération, les deux événements Complete sont appelés comme dans les exemples précédents.

## <a name="unpaired-event-handlers"></a>Gestionnaires d’événements

Tant que l’état passé à l’événement n’est pas **adStatusCantDeny**, vous pouvez désactiver les notifications d’événements des événements en renvoyant la **valeur adStatusUnwantedEvent** dans le paramètre *Status* . Par exemple, lors du premier appel du gestionnaire d'événements Complete, vous pouvez retourner **adStatusUnwantedEvent**. Vous ne recevrez par la suite que les événements Will. Cependant, certains événements peuvent être déclenchés pour plus d'une raison. Dans ce cas, l’événement aura un paramètre *Reason* . Lorsque vous retournez **adStatusUnwantedEvent**, vous ne recevrez plus de notifications pour cet événement s'il se produit pour la raison définie. En d'autres termes, il se peut que vous receviez une notification pour chaque autre raison déclenchant l'événement.

Dans certains cas, les gestionnaires d'événements Will uniques sont utiles pour examiner les paramètres utilisés dans une opération. Vous pouvez modifier ces paramètres d'opération ou annuler l'opération

Vous pouvez également conserver la notification d'événements Complete activée. Lorsque le premier gestionnaire d'événements Will est appelé, retournez **adStatusUnwantedEvent**. Vous ne recevrez par la suite que les événements Complete.

Les gestionnaires d'événements Complete uniques peuvent être utiles pour gérer les opérations asynchrones. Chaque opération asynchrone est associée à un événement Complete approprié.

Par exemple, le remplissage d'un objet [Recordset](recordset-object-ado.md) volumineux peut être long. Si votre application est correctement écrit, vous pouvez démarrer une opération et poursuivre le traitement des autres. Vous serez averti de la fin du remplissage de l'objet **Recordset** par un événement **ExecuteComplete**.

## <a name="single-event-handlers-and-multiple-objects"></a>Gestionnaires d’événements uniques et objets multiples

La souplesse d'un langage de programmation tel que Microsoft Visual C++ vous permet de n'utiliser qu'un gestionnaire pour traiter les événements liés à plusieurs objets. Par exemple, vous pouvez n'avoir qu'un seul gestionnaire d'événements **Disconnect** pour traiter les événements de plusieurs objets **Connection**. Si l'une des connexions se termine, le gestionnaire d'événements **Disconnect** est appelé. Vous pouvez déterminer la connexion à l'origine de l'événement, car le paramètre d'objet du gestionnaire d'événements sera défini avec l'objet **Connection** correspondant

> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas utiliser cette technique en Visual Basic, car ce langage ne peut associer qu'un seul objet à un gestionnaire d'événements.


