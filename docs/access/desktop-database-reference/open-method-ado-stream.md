---
title: Open, méthode (flux ADO)
TOCTitle: Open method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a943209ce329d59fb4846ed18fd008bc45803da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715542"
---
# <a name="open-method-ado-stream"></a>Open, méthode (flux ADO)


**S’applique à**: Access 2013, Office 2013


Ouvre un objet [Stream](stream-object-ado.md) pour manipuler des flux de données binaires ou de texte.

## <a name="syntax"></a>Syntaxe

*Flux de données*. Ouvrir la *Source*, le *Mode*, *Si OptionsOuverture a*, *nom d’utilisateur*, *mot de passe*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **Variant** qui spécifie la source de données de l'objet **Stream**. *Source* peut contenir une chaîne d’URL absolue qui pointe vers un nœud existant dans une arborescence connue, comme un système de fichiers ou de messagerie. Une URL doit être spécifiée à l’aide du mot clé URL (« URL =*schéma*://*server*/*dossier*»). *Source* peut également contenir une référence à un objet [Record](record-object-ado.md) déjà ouvert, qui ouvre le flux par défaut associé à l' **enregistrement**. Si la *Source* n’est pas spécifié, un **flux de données** est instancié et ouvert, associé à aucune source sous-jacente par défaut. Pour plus d’informations sur les schémas d’URL et leurs fournisseurs associés, consultez [URL absolues et relatives](absolute-and-relative-urls.md).|
|*Mode* |Facultatif. Valeur [ConnectModeEnum](connectmodeenum.md) qui spécifie le mode d'accès de l'objet **Stream** résultant (par exemple, lecture/écriture ou en lecture seule). La valeur par défaut est **adModeUnknown**. Pour plus d'informations sur les modes d'accès, consultez la propriété [Mode](mode-property-ado.md). Si *Mode* n’est pas spécifié, il est hérité de l’objet source. Par exemple, si l'objet **Record** source est ouvert en lecture seule, l'objet **Stream** sera également ouvert en lecture seule par défaut.|
|*Si OptionsOuverture a* |Facultatif. Valeur [StreamOpenOptionsEnum](streamopenoptionsenum.md). La valeur par défaut est **adOpenStreamUnspecified**.|
|*UserName* |Facultatif. Valeur de type **String** contenant l'ID utilisateur qui, le cas échéant, accède à l'objet **Stream**.|
|*MotDePasse* |Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, accède à l'objet **Stream**.|

## <a name="remarks"></a>Notes

Lorsqu’un objet **Record** est passé comme paramètre source, le *nom d’utilisateur* et les paramètres de *mot de passe* ne permettent pas, car l’accès à l’objet **Record** est déjà disponible. De même, le [Mode](mode-property-ado.md) de l’objet **Record** est transféré vers l’objet **Stream** . Lors de la *Source* n’est pas spécifié, le **flux** ouvert ne contient aucune donnée et possède une [taille](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de zéro (0). Pour éviter de perdre des données qui sont écrites dans ce **flux** lorsque le **flux** est fermé, enregistrez le **flux de données** avec les méthodes [CopyTo](copyto-method-ado.md) ou [SaveToFile](savetofile-method-ado.md) , ou enregistrez-le dans un autre emplacement de la mémoire.

Une valeur *Si OptionsOuverture a* **adOpenStreamFromRecord** identifie le contenu du paramètre *Source* est un objet **Record** déjà ouvert. Le comportement par défaut consiste à traiter *Source* comme une URL qui pointe directement vers un nœud dans une arborescence, tel qu’un fichier. Le flux par défaut associé à ce nœud est ouvert.

Pendant que le **flux de données** n’est pas ouvert, il est possible de lire toutes les propriétés en lecture seule du **flux**. Si un **flux** est ouvert de façon asynchrone, toutes les opérations suivantes (autres que la vérification de l' [état](state-property-ado.md) et autres propriétés en lecture seule) sont bloquées jusqu'à ce que l’opération **d’ouverture** est terminée.

Outre les options présentées ci-dessus, l’omission de *Source* vous permet d’instancier simplement un objet **Stream** en mémoire sans l’associer à une source sous-jacente. Vous pouvez ajouter dynamiquement des données à un flux en écrivant des données binaires ou de texte dans l’objet **Stream** avec les méthodes [Write](write-method-ado.md) ou [WriteText](writetext-method-ado.md), ou en chargeant les données d’un fichier à l’aide de la méthode [LoadFromFile](loadfromfile-method-ado.md).

