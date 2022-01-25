---
title: Fonctions asynchrones définies par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
ms.openlocfilehash: 5a97e8d43f4800c93a3f1d59ba34fc52ccf77e60
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198995"
---
# <a name="asynchronous-user-defined-functions"></a>Fonctions asynchrones définies par l’utilisateur

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 peut appeler des fonctions définies par l’utilisateur de manière asynchrone. L’appel asynchrone de fonctions peut améliorer les performances en permettant l’exécution de plusieurs calculs en même temps. Lorsque vous exécutez des fonctions définies par l’utilisateur sur un cluster de calcul, le fait d’appeler les fonctions de manière asynchrone permet de pouvoir utiliser plusieurs ordinateurs pour effectuer les calculs.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Quand utiliser des fonctions asynchrones définies par l’utilisateur

Certaines fonctions définies par l’utilisateur doivent attendre des ressources externes. Pendant qu’ils attendent, le thread Excel de calcul est bloqué. Dans Excel 2013, les fonctions définies par l’utilisateur peuvent s’exécuter de manière asynchrone. Cela permet au thread de calcul d’exécuter d’autres calculs pendant que la fonction définie par l’utilisateur attend.
  
Dans Excel 2007, les programmeurs pouvaient exécuter plusieurs fonctions définies par l’utilisateur en même temps en augmentant le nombre de threads utilisés dans les recalculs à plusieurs threads. Cette méthode présente des inconvénients principalement car le nombre de threads est un paramètre d’étendue à une application et ne peut pas être contrôlé au niveau d’une fonction unique ou d’un add-in.
  
Les programmeurs doivent utiliser des appels de fonction asynchrone définis par l’utilisateur lorsque la fonction doit attendre des ressources externes. Par exemple, une fonction qui envoie une demande SOAP sur Internet doit attendre que le réseau envoie la demande, que le serveur distant termine la demande et que le réseau renvoie le résultat. Dans ce cas, aucun calcul significatif ne se produit et les Excel peuvent continuer avec d’autres calculs.
  
Les programmeurs peuvent également utiliser des fonctions asynchrones définies par l’utilisateur lorsqu’une fonction envoie des demandes à un cluster de calcul. Dans ce cas, il n’y a pas seulement une latence réseau à attendre, mais le cluster peut exécuter des appels distincts sur des serveurs distincts. En n’attendant pas la fin de chaque appel, les appels peuvent être superposés pour améliorer les performances. Dans certains cas, cette amélioration est significative.
  
> [!NOTE]
> Les fonctions définies par l’utilisateur ne peuvent pas être enregistrées en tant qu’fonctions asynchrones et sécurisées pour le cluster. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Écriture d’une fonction asynchrone définie par l’utilisateur

Les fonctions asynchrones définies par l’utilisateur doivent assurer le suivi d’un handle et l’utiliser lors de l’Excel que l’appel de fonction est terminé. Une fonction asynchrone définie par l’utilisateur est divisée en deux parties. La première partie est le point d’entrée UDF standard, qui lance une deuxième opération asynchrone distincte. Les rappels dans Excel doivent être effectués pendant le point d’entrée UDF. La première partie de lancement de la fonction retourne ensuite le contrôle de son thread de calcul à Excel, qui poursuit le calcul. Lorsque la deuxième opération asynchrone est terminée, elle doit rappeler dans Excel et fournir Excel avec son résultat. 
  
> [!NOTE]
> Tous les arguments transmis à l’UDF qui sont nécessaires à la partie asynchrone de la fonction doivent être copiés en profondeur, car Excel libère ces arguments lorsque le point d’entrée UDF renvoie. 
  
Excel fournit un ensemble d’événements qu’un add-in XLL peut utiliser pour gérer le cycle de vie des appels UDF asynchrones. Ces événements indiquent que Excel est terminé avec des calculs ou que le calcul a été annulé.
  
### <a name="declaring-an-asynchronous-function"></a>Déclaration d’une fonction asynchrone

Vous devez déclarer des fonctions asynchrones définies par l’utilisateur comme asynchrones lorsqu’elles sont inscrites. Pour ce faire, vous ajoutez un paramètre qui pointe vers une structure XLOPER12, représentée par « X » dans la chaîne du type d’inscription, n’importe où dans la liste des paramètres UDF. Excel utilise ce paramètre pour transmettre le handle d’appel asynchrone. Le add-in XLL doit transmettre le handle d’appel asynchrone et le résultat de la fonction à Excel lorsque le résultat est prêt. En outre, le type de retour de l’UDF doit être **nul,** désigné par « > » comme premier caractère de la chaîne de type. Le type de retour est nul car la partie synchrone de l’UDF ne retourne pas de valeur à Excel. Au lieu de cela, le add-in XLL renvoie une valeur de manière asynchrone par le biais d’un rappel. 
  
Vous pouvez déclarer des fonctions asynchrones comme thread-safe, puis la partie synchrone de l’UDF est utilisée dans un recalcul multi-thread. 
  
L’exemple de code suivant montre une fonction asynchrone définie par l’utilisateur enregistrée à l’aide de « QX » comme chaîne de \> type d’inscription :
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Renvoi de valeurs

Lorsque le résultat de l’appel asynchrone est prêt, le add-in XLL renvoie le résultat à Excel en faisant un rappel de type [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** est le seul rappel que vous pouvez utiliser sur des threads autres que des threads de calcul lors du recalcul. Par conséquent, la partie asynchrone d’une UDF asynchrone ne doit pas effectuer d’autres rappels. 
  
### <a name="handling-events"></a>Traitement des événements

À compter Excel 2010, les XL peuvent recevoir des événements conçus pour gérer le cycle de vie de la fonction asynchrone. Pour plus d’informations, voir [Gestion des événements.](handling-events.md)
  
## <a name="see-also"></a>Voir aussi

- [Développement de XLL de Excel 2013](developing-excel-xlls.md)

