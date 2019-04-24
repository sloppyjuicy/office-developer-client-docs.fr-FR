---
title: Implémentation des objets dans C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310149"
---
# <a name="implementing-objects-in-c"></a>Implémentation des objets dans C++

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services et les clients C++ définissent les objets MAPI en créant des classes qui héritent des interfaces qu'ils implémentent. Chacune des méthodes d'interface est public, de même que le constructeur et le destructeur de la classe. Si la classe possède des méthodes supplémentaires, elles peuvent être publiques ou privées, en fonction de l'implémentation. Tous les membres de données sont privés. 
  
L'exemple de code suivant montre comment définir un objet d'État C++. La `CMyMAPIObject` classe hérite de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . De nombreuses macros utilisées dans cet exemple sont définies dans le fichier d'en-tête OLE compobj. h. Les premiers membres de la classe sont les méthodes de l'interface de base, suivies des méthodes des interfaces héritées par ordre d'héritage. Le suivi des définitions d'interface est une méthode supplémentaire, le constructeur et le destructeur, ainsi que les membres de données. 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

Pour utiliser une instance de la `CMyMAPIObject` classe, les clients C++ ou les fournisseurs de services effectuent un appel à l'une de ses méthodes comme suit: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Voir aussi

- [Implémentation d'objets MAPI](implementing-mapi-objects.md)

