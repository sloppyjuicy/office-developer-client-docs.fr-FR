---
title: 'Chapitre 6 : Gérer des erreurs'
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7fd97104be4563b0245aac97f37aa1158d0463fa
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860412"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="0e718-102">Chapitre 6 : Gérer des erreurs</span><span class="sxs-lookup"><span data-stu-id="0e718-102">Chapter 6: Error Handling</span></span>


<span data-ttu-id="0e718-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e718-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0e718-p101">ADO utilise différentes méthodes pour avertir une application d'une erreur. Ce chapitre présente les types d'erreurs pouvant survenir lorsque vous utilisez ADO et comment votre application est avertie. Différentes façons de gérer ces erreurs sont également suggérées en fin de chapitre.</span><span class="sxs-lookup"><span data-stu-id="0e718-p101">ADO uses several different methods to notify an application of errors that occur. This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified. It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="0e718-107">Comment ADO signale-t-il les erreurs ?</span><span class="sxs-lookup"><span data-stu-id="0e718-107">How Does ADO Report Errors?</span></span>

<span data-ttu-id="0e718-108">ADO vous avertit des erreurs de diverses façons :</span><span class="sxs-lookup"><span data-stu-id="0e718-108">ADO notifies you about errors in several ways:</span></span>

  - <span data-ttu-id="0e718-p102">Les erreurs ADO génèrent une erreur d'exécution. Vous pouvez gérer une erreur ADO de la même manière que toute autre erreur d'exécution, en utilisant une instruction **Sur erreur** dans Visual Basic, par exemple.</span><span class="sxs-lookup"><span data-stu-id="0e718-p102">ADO errors generate a run-time error. Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

  - <span data-ttu-id="0e718-p103">Votre programme peut recevoir des erreurs de la base de données OLE DB. Ce type d'erreur génère également une erreur d'exécution.</span><span class="sxs-lookup"><span data-stu-id="0e718-p103">Your program can receive errors from OLE DB. An OLE DB error generates a run-time error as well.</span></span>

  - <span data-ttu-id="0e718-113">Si l'erreur est propre à votre fournisseur de données, un ou plusieurs objets **Error** sont placés dans la collection **Errors** de l'objet **Connection** utilisé pour accéder au magasin de données au moment de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="0e718-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

  - <span data-ttu-id="0e718-p104">Si le processus à l'origine d'un événement provoque aussi une erreur, les informations relatives à cette dernière sont placées dans un objet **Error** et transférées comme paramètre à l'événement. Reportez-vous au [Chapitre 7 : Gestion des événements ADO](chapter-7-handling-ado-events.md) pour en savoir plus sur les événements.</span><span class="sxs-lookup"><span data-stu-id="0e718-p104">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event. See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

  - <span data-ttu-id="0e718-p105">Les problèmes qui surviennent pendant le traitement de mises à jour en lot ou d'autres opérations de masse impliquant un **jeu d'enregistrements** peuvent être signalés par la propriété **Status** du **jeu d'enregistrements**. Par exemple, les violations de restrictions de schémas ou des autorisations insuffisantes peuvent être spécifiées par des valeurs **RecordStatusEnum**.</span><span class="sxs-lookup"><span data-stu-id="0e718-p105">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**. For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

  - <span data-ttu-id="0e718-p106">Les problèmes impliquant un **champ** particulier dans l'enregistrement actif sont également signalés par la propriété **Status** de chaque **champ** de la collection **Fields** de l' **enregistrement** ou du **jeu d'enregistrements**. Par exemple, les mises à jour interrompues ou les types de données incompatibles peuvent être spécifiés par les valeurs **FieldStatusEnum**.</span><span class="sxs-lookup"><span data-stu-id="0e718-p106">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**. For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="0e718-120">Les sections ci-après décrivent plus en détail chacune de ces méthodes de notification.</span><span class="sxs-lookup"><span data-stu-id="0e718-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="0e718-121">Erreurs ADO</span><span class="sxs-lookup"><span data-stu-id="0e718-121">ADO Errors</span></span>](ado-errors.md)

- [<span data-ttu-id="0e718-122">Référence des erreurs ADO</span><span class="sxs-lookup"><span data-stu-id="0e718-122">ADO Error Reference</span></span>](ado-error-reference.md)

- [<span data-ttu-id="0e718-123">Erreurs de fournisseur</span><span class="sxs-lookup"><span data-stu-id="0e718-123">Provider Errors</span></span>](provider-errors.md)

- [<span data-ttu-id="0e718-124">Informations sur les erreurs en lien avec le champ</span><span class="sxs-lookup"><span data-stu-id="0e718-124">Field-Related Error Information</span></span>](field-related-error-information.md)

- [<span data-ttu-id="0e718-125">Informations sur les erreurs en lien avec le recordset</span><span class="sxs-lookup"><span data-stu-id="0e718-125">Recordset-Related Error Information</span></span>](recordset-related-error-information.md)

- [<span data-ttu-id="0e718-126">Anticipation des erreurs</span><span class="sxs-lookup"><span data-stu-id="0e718-126">Anticipating Errors</span></span>](anticipating-errors.md)

- [<span data-ttu-id="0e718-127">Handling Errors in Other Languages (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e718-127">Handling Errors in Other Languages (ADO)</span></span>](handling-errors-in-other-languages.md)