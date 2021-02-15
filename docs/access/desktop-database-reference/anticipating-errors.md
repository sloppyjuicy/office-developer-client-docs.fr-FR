---
title: Anticipation des erreurs
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4bd130ca05527c7761ca587781c1fd4f939ebe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297170"
---
# <a name="anticipating-errors"></a><span data-ttu-id="75045-102">Anticipation des erreurs</span><span class="sxs-lookup"><span data-stu-id="75045-102">Anticipating errors</span></span>


<span data-ttu-id="75045-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75045-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75045-p101">La prévention des erreurs est tout aussi importante que leur gestion. Cette dernière section contient une courte liste des précautions à prendre dans votre application pour réduire le nombre d'erreurs éventuelles.</span><span class="sxs-lookup"><span data-stu-id="75045-p101">Error prevention is at least as important as error handling. This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="75045-p102">Vérifiez l'état des objets en contrôlant la valeur de la propriété **State** avant d'exécuter une opération avec ces objets. Par exemple, si votre application utilise un objet **Connection** global, vérifiez sa propriété **State** pour savoir s'il est déjà ouvert avant d'appeler la méthode **Open**.</span><span class="sxs-lookup"><span data-stu-id="75045-p102">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects. For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

- <span data-ttu-id="75045-p103">Tout programme qui accepte des données d'un utilisateur doit inclure du code visant à valider les données avant de les envoyer au magasin de données. Vous ne pouvez pas compter sur le magasin de données, le fournisseur, ADO ou même votre langage de programmation pour signaler des problèmes. Vous devez vérifier chaque octet entré par vos utilisateurs et vous assurer que les données des champs sont correctes et que les champs obligatoires ne sont pas vides.</span><span class="sxs-lookup"><span data-stu-id="75045-p103">Any program that accepts data from a user must include code to validate that data before sending it to the data store. You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems. You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="75045-p104">Vérifiez les données avant d'essayer de les inscrire dans un magasin de données. Pour ce faire, la méthode la plus simple consiste à gérer les événements **WillMove** ou **WillUpdateRecordset**. Pour une explication plus complète de la gestion des événements ADO, consultez le [chapitre 7 : Gestion des événements ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="75045-p104">Check the data before you try to write any data to the data store. The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="75045-p105">Assurez-vous que les objets **Record** ne sont pas en dehors des limites de l'objet **Recordset** avant de déplacer le pointeur d'enregistrements. Si vous essayez d'exécuter la méthode **MoveNext** lorsque la propriété **EOF** a la valeur True ou **MovePrev** lorsque la propriété **BOF** a la valeur True, une erreur se produit. Si vous exécutez les méthodes **Move** lorsque les propriétés **EOF** et **BOF** ont la valeur True, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="75045-p105">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="75045-117">Des erreurs se produisent si vous essayez d'effectuer des opérations, telles que **Seek** et **Find** sur un objet **Recordset** vide.</span><span class="sxs-lookup"><span data-stu-id="75045-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

