---
title: Fonctions asynchrones définies par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5b64dfd4308da4efb5e94010fe1dc9d758a1199c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782001"
---
# <a name="asynchronous-user-defined-functions"></a>Fonctions asynchrones définies par l’utilisateur

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 peuvent appeler des fonctions définies par l’utilisateur en mode asynchrone. Appeler des fonctions de manière asynchrone peut améliorer les performances en autorisant plusieurs calculs à exécuter en même temps. Lorsque vous exécutez des fonctions définies par l’utilisateur sur un cluster de calcul, appeler des fonctions de manière asynchrone permet à plusieurs ordinateurs à utiliser pour effectuer les calculs.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Quand utiliser des fonctions asynchrones définies par l’utilisateur

Certaines fonctions définies par l’utilisateur doivent attendre des ressources externes. Pendant qu’ils attendent, le thread de calcul Excel est bloqué. Dans Excel 2013, les fonctions définies par l’utilisateur peuvent exécuter de façon asynchrone. Cela libère le thread de calcul pour exécuter d’autres calculs pendant que la fonction définie par l’utilisateur en attente.
  
Dans Excel 2007, les programmeurs peuvent exécuter plusieurs fonctions définies par l’utilisateur en même temps en augmentant le nombre de threads utilisés dans plusieurs threads recalculs. Cette méthode présente les inconvénients principalement parce que le nombre de threads est un paramètre étendu à une application et ne peut pas être contrôlé au niveau d’une seule fonction ou une macro complémentaire.
  
Programmeurs doivent utiliser des appels asynchrones de fonction définie par l’utilisateur lors de la fonction doit attendre des ressources externes. Par exemple, une fonction qui envoie une demande SOAP via Internet doit attendre le réseau fournir la demande, le serveur distant pour effectuer la demande et du réseau pour renvoyer le résultat. Dans ce cas, il n’existe aucun produit informatique significative et Excel peut continuer à d’autres calculs.
  
Ils peuvent également utiliser des fonctions asynchrones définies par l’utilisateur lorsqu’une fonction envoie des demandes à un cluster de calcul. Dans ce cas, il n’est pas uniquement latence du réseau d’attendre, mais le cluster peut exécuter des appels séparés sur des serveurs distincts. Sans attendre que chaque appel à la fin, les appels peuvent être superposés pour améliorer les performances. Dans certains cas, cette amélioration est importante.
  
> [!NOTE]
> Fonctions définies par l’utilisateur ne peut pas être enregistrées en tant que les deux asynchrone et sans échec du cluster. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Écrire une fonction asynchrone définie par l’utilisateur

Des fonctions asynchrones définies par l’utilisateur doivent suivre une poignée et utilisez ce handle en informant Excel que l’appel de fonction est terminée. Une fonction définie par l’utilisateur asynchrone est divisée en deux. La première partie est le point d’entrée UDF standard, qui lance une opération asynchrone de deuxième et distincte. Rappels dans Excel doivent être effectuées pendant le point d’entrée UDF. La première partie de lancement de la fonction retournera puis contrôle de son thread de calcul dans Excel, qui continue de calcul. Lors de la deuxième opération asynchrone est terminée, il doit rappeler dans Excel et fournir Excel par son résultat. 
  
> [!NOTE]
> Tous les arguments transmis dans le fichier UDF sont requis par la partie asynchrone la fonction doit être approfondie copiés car Excel libère de ces arguments retourne le point d’entrée UDF. 
  
Excel propose un ensemble d’événements qu’un complément XLL permettre utiliser pour gérer le cycle de vie d’appels UDF asynchrones. Ces événements indiquent que Excel est terminé avec calculs ou que le calcul a été annulé.
  
### <a name="declaring-an-asynchronous-function"></a>Déclaration d’une fonction asynchrone

Vous devez déclarer des fonctions asynchrones définies par l’utilisateur comme asynchrone lorsqu’ils sont enregistrés. Cette opération est effectuée en ajoutant un paramètre qui pointe vers une structure XLOPER12, représenté par « X » dans la chaîne de type d’enregistrement, n’importe où dans la liste des paramètres UDF. Excel utilise ce paramètre pour transmettre le handle de l’appel asynchrone. Le complément XLL doit transmettre le descripteur d’appel asynchrone et le résultat de la fonction dans Excel lorsque le résultat est prêt. En outre, le type de retour de l’UDF doit être **void**, désigné par « > » en tant que le premier caractère de la chaîne du type. Le type de retour est void, car la partie synchrone de l’UDF ne retourne pas une valeur pour Excel. Au lieu de cela, le complément XLL renvoie une valeur de manière asynchrone par le biais d’un rappel. 
  
Vous pouvez déclarer des fonctions asynchrones en tant que thread-safe et, le composant de l’UDF synchrone est utilisé dans un recalcul multi-thread. 
  
L’exemple de code suivant montre une fonction asynchrone définie par l’utilisateur inscrite à l’aide de «\>QX » en tant que la chaîne du type d’enregistrement :
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Renvoi de valeurs

Lorsque le résultat de l’appel asynchrone est prêt, le complément XLL renvoie le résultat dans Excel en effectuant un rappel de type [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** est le rappel seulement que vous pouvez utiliser sur des threads non calcul pendant le recalcul. Par conséquent, la partie d’une fichier UDF asynchrone asynchrone ne doit pas effectuer tous les rappels. 
  
### <a name="handling-events"></a>Gestion d'événements

À compter d’Excel 2010, XLL peuvent recevoir des événements conçus pour gérer le cycle de vie de fonction asynchrone. Pour plus d’informations, voir [Gestion des événements](handling-events.md).
  
## <a name="see-also"></a>Voir aussi

- [D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

