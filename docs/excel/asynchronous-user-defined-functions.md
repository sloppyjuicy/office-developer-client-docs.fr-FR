---
title: Fonctions asynchrones définies par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7fdf3bd09914981865c911fd65a78d044ad582f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412309"
---
# <a name="asynchronous-user-defined-functions"></a>Fonctions asynchrones définies par l’utilisateur

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 peut appeler des fonctions définies par l'utilisateur de manière asynchrone. L'appel de fonctions de manière asynchrone peut améliorer les performances en autorisant l'exécution de plusieurs calculs en même temps. Lorsque vous exécutez des fonctions définies par l’utilisateur sur un cluster de calcul, le fait d’appeler les fonctions de manière asynchrone permet de pouvoir utiliser plusieurs ordinateurs pour effectuer les calculs.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Quand utiliser des fonctions asynchrones définies par l'utilisateur

Certaines fonctions définies par l'utilisateur doivent attendre les ressources externes. Lorsqu'elles attendent, le thread de calcul Excel est bloqué. Dans Excel 2013, les fonctions définies par l'utilisateur peuvent s'exécuter de manière asynchrone. Cela permet de libérer le thread de calcul pour exécuter d'autres calculs pendant que la fonction définie par l'utilisateur attend.
  
Dans Excel 2007, les programmeurs pouvaient exécuter simultanément plusieurs fonctions définies par l'utilisateur en augmentant le nombre de threads utilisés dans les recalculs à plusieurs threads. Cette méthode présente des inconvénients principalement, car le nombre de threads est un paramètre étendu à une application et ne peut pas être contrôlé au niveau d'une fonction unique ou d'un complément.
  
Les programmeurs doivent utiliser des appels asynchrones de fonctions définies par l'utilisateur lorsque la fonction doit attendre des ressources externes. Par exemple, une fonction qui envoie une demande SOAP sur Internet doit attendre que le réseau remette la demande, le serveur distant pour effectuer la demande et le réseau pour renvoyer le résultat. Dans ce cas, il n'y a pas de calcul significatif et Excel peut poursuivre les autres calculs.
  
Les programmeurs peuvent également utiliser des fonctions asynchrones définies par l'utilisateur lorsqu'une fonction envoie des demandes à un cluster de calcul. Dans ce cas, la latence du réseau est insuffisante, mais le cluster peut exécuter des appels distincts sur des serveurs distincts. En n'attendant pas que chaque appel se termine, les appels peuvent être superposés pour améliorer les performances. Dans certains cas, cette amélioration est importante.
  
> [!NOTE]
> Les fonctions définies par l'utilisateur ne peuvent pas être inscrites en tant que Asynchronous et cluster safe. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Écriture d'une fonction définie par l'utilisateur asynchrone

Les fonctions asynchrones définies par l'utilisateur doivent assurer le suivi d'un handle et utiliser ce handle pour informer Excel de la fin de l'appel de fonction. Une fonction définie par l'utilisateur asynchrone est divisée en deux parties. La première partie est le point d'entrée UDF standard, qui lance une seconde opération asynchrone distincte. Les rappels dans Excel doivent être effectués pendant le point d'entrée UDF. La première partie de lancement de la fonction renverra ensuite le contrôle de son thread de calcul dans Excel, qui poursuivra le calcul. Lorsque la deuxième opération asynchrone est terminée, elle doit effectuer un rappel dans Excel et fournir le résultat Excel. 
  
> [!NOTE]
> Tout argument transmis à la FDU et nécessaire par la partie asynchrone la fonction doit être copiée en profondeur, car Excel libère ces arguments lorsque le point d'entrée UDF renvoie. 
  
Excel fournit un ensemble d'événements qu'un complément XLL peut utiliser afin de gérer le cycle de vie des appels UDF asynchrones. Ces événements indiquent qu'Excel a terminé les calculs ou que le calcul a été annulé.
  
### <a name="declaring-an-asynchronous-function"></a>Déclaration d'une fonction asynchrone

Vous devez déclarer des fonctions asynchrones définies par l'utilisateur comme asynchrones lorsqu'elles sont inscrites. Cette opération est effectuée en ajoutant un paramètre qui pointe vers une structure XLOPER12, représentée par «X» dans la chaîne de type d'enregistrement, dans la liste des paramètres UDF. Excel utilise ce paramètre pour transmettre le handle d'appel asynchrone. Le complément XLL doit transmettre le handle d'appel asynchrone et le résultat de la fonction à Excel lorsque le résultat est prêt. En outre, le type de retour de la FDU doit être **void**, désigné par «>» comme premier caractère de la chaîne de type. Le type de retour est void car la partie synchrone de la FDU ne renvoie pas de valeur à Excel. Au lieu de cela, le complément XLL renvoie une valeur de manière asynchrone via un rappel. 
  
Vous pouvez déclarer des fonctions asynchrones en tant que thread-safe, puis la partie synchrone de la FDU est utilisée dans un recalcul multi-thread. 
  
L'exemple de code suivant montre une fonction définie par l'utilisateur asynchrone inscrite\>à l'aide de «qx» comme chaîne de type d'enregistrement:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Renvoi de valeurs

Lorsque le résultat de l'appel asynchrone est prêt, le complément XLL renvoie le résultat à Excel en exécutant un rappel de type [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** est le seul rappel que vous pouvez utiliser sur les threads de non calcul lors du recalcul. Par conséquent, la partie asynchrone d'une FDU asynchrone ne doit pas effectuer d'autres rappels. 
  
### <a name="handling-events"></a>Gestion des événements

À partir d'Excel 2010, les XLL peuvent recevoir des événements conçus pour gérer le cycle de vie des fonctions asynchrones. Pour plus d'informations, consultez la rubrique [gestion des événements](handling-events.md).
  
## <a name="see-also"></a>Voir aussi

- [Développement de XLL de Excel](developing-excel-xlls.md)

