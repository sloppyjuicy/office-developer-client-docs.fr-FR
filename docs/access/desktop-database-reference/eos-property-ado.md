---
title: EOS, propriété (ADO - référence du bureau de la base de données Access))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470699"
---
# <a name="eos-property-ado"></a>EOS, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique si la position actuelle est à la fin du flux.

## <a name="return-values"></a>Valeurs renvoyées

Renvoie une valeur **booléenne** qui indique si la position actuelle est à la fin du flux. **EOS** renvoie **True** s'il ne reste plus d'octets dans le flux ; il renvoie **False** s'il reste des octets après la position actuelle.

Pour définir la position de fin de flux, utilisez la méthode [SetEOS](seteos-method-ado.md). Pour déterminer la position actuelle, utilisez la propriété [Position](position-property-ado.md).

