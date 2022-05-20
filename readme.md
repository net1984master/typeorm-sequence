# Typeorm-sequence ........................[Original author Ian Oliveira](https://github.com/ianprogrammer/typeorm-sequence "Original")

Typeorm-sequence is a library that enables you to use a db sequence in a column (it works only on postgres and oracle yet).

# Install via NPM

```
  npm i typeorm-sequence-oracle-fixed
```

# Usage

```
import { Entity, Column, PrimaryColumn } from 'typeorm'
import { NextVal, EntityWithSequence } from 'typeorm-sequence-oracle-fixed'

@Entity({ name: 'client_table' })
export class Client extends EntityWithSequence {

  @NextVal('seq_client')
  @PrimaryColumn({ name: 'client_id' })
  id: number

  @Column({ name: 'client_name' })
  name: string
  constructor() {
    super()
  }
}
```
