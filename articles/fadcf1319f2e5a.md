---
title: "ts 勉強メモ"
emoji: "🎉"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["typescript",  ""]
published: false
---


```typescript

    //-------------------------------------------------------------------
    // 文字列がnull,undefined,空文字の場合
    // または数値がnull,undefined,0の場合Trueを返す
    public static isFalsy(arg: string): arg is '' | undefined | null;
    public static isFalsy(arg: number): arg is 0 | undefined | null;
    public static isFalsy(arg: boolean): arg is false | undefined | null;
    /* eslint-disable @typescript-eslint/explicit-module-boundary-types,@typescript-eslint/no-explicit-any*/
    public static isFalsy(arg: any): arg is undefined | null; // 外部APIで実装されている複合型用
    public static isFalsy(arg: any): arg is '' | 0 | false | undefined | null {
        if (arg == undefined) return true;
        if (arg === '') return true;
        if (arg === false) return true;
        if (arg === 0) return true;
        return false;
    }
```



