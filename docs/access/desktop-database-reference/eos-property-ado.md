---
title: Propriété EOS (ADO - Référence de base de données de bureau Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3c32f2794014a05fa45589780447100298adf88d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585710"
---
# <a name="eos-property-ado"></a>EOS, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique si la position actuelle est à la fin du flux.

## <a name="return-values"></a>Valeurs de retour

Renvoie une valeur **booléenne** qui indique si la position actuelle est à la fin du flux. **EOS** renvoie **True** s'il ne reste plus d'octets dans le flux ; il renvoie **False** s'il reste des octets après la position actuelle.

Pour définir la position de fin de flux, utilisez la méthode [SetEOS](seteos-method-ado.md). Pour déterminer la position actuelle, utilisez la propriété [Position](position-property-ado.md).

