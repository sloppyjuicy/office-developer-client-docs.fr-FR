---
title: Définition d'un verrou (Référence de base de données du bureau access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f852901be41060568bdbad539906e9166d080fad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470938"
---
# <a name="what-is-a-lock"></a>Définition d'un verrou


**S’applique à**: Access 2013 | Office 2013

Le verrouillage est le processus par lequel un SGBD limite l'accès à une ligne dans un environnement multi-utilisateur. Lorsqu'une ligne ou une colonne est verrouillée en mode exclusif, les autres utilisateurs ne sont pas autorisés à accéder aux données avant que le verrou soit libéré. Il s'agit d'une procédure de sécurité qui permet d'éviter la mise à jour simultanée de la même colonne d'une ligne par deux utilisateurs.

Les verrous peuvent s'avérer très coûteux en termes de ressources. Il est donc conseillé de les utiliser dans le seul cas où il est impératif de préserver l'intégrité des données. Dans une base de données où des centaines, voire des milliers d'utilisateurs, sont susceptibles d'accéder aux enregistrements à chaque seconde, par exemple une base de données connectée à Internet, un verrouillage superflu peut rapidement engendrer un ralentissement des performances de l'application.

Vous pouvez contrôler la façon dont la source de données et la bibliothèque de curseurs ADO gèrent l'accès concurrentiel en choisissant l'option de verrouillage appropriée.

Définissez la propriété **LockType** avant d'ouvrir un objet **Recordset** pour spécifier le type de verrouillage que le fournisseur doit utiliser pour son ouverture. Lisez la propriété pour obtenir le type de verrouillage actuellement utilisé sur un objet **Recordset** ouvert.

Certains fournisseurs ne prennent pas tous les types de verrou en charge. Si un fournisseur ne prend pas en charge le paramètre **LockType** requis, il lui substituera automatiquement un autre type de verrou. Utilisez la méthode **Supports** avec [adUpdate](supports-method-ado.md) et **adUpdateBatch** pour déterminer les fonctionnalités de verrouillage disponibles dans un objet **Recordset**.

Le paramètre **adLockPessimistic** n'est pas pris en charge si la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**. Si vous définissez une valeur non prise en charge, aucune erreur n'est générée ; elle sera simplement remplacée par la valeur de **LockType** la plus similaire prise en charge.

La propriété **LockType** est accessible en lecture/écriture lorsque l'objet **Recordset** est fermé, et en lecture seule lorsqu'il est ouvert.

